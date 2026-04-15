# Zentto — Org Security Workflow

Este repositorio (`zentto-erp/.github`) hospeda el **reusable workflow de seguridad** que aplica a todos los repositorios de la organización.

## Herramientas incluidas

| Herramienta | Cobertura |
|---|---|
| **Semgrep** (OSS) | SAST: SSRF, SQLi, XSS, CSRF, command injection, ReDoS, rate limiting, path traversal, secretos en código. Rulesets `p/ci`, `p/security-audit`, `p/owasp-top-ten`, `p/javascript`, `p/typescript`, `p/nodejs`, `p/expressjs`, `p/github-actions`, `p/dockerfile`, `p/secrets`. |
| **Gitleaks** | Secretos en historial git completo (tokens, keys, passwords). |
| **Trivy** | CVEs de dependencias (npm, Go, Python), Dockerfiles e IaC (Terraform, K8s). |
| **OSV-Scanner** (Google) | CVEs cross-ecosystem vía la base OSV. |
| **zizmor** | Auditoría de GitHub Actions: permisos faltantes, script injection, leak de secrets, untrusted checkout. |
| **actionlint** | Sintaxis y best practices en workflows. |

## Uso desde un repo consumidor

Crear `.github/workflows/security.yml`:

```yaml
name: Security

on:
  push:
    branches: [main, developer, master]
  pull_request:
    branches: [main, developer, master]
  schedule:
    - cron: '0 6 * * 1'
  workflow_dispatch:

permissions:
  contents: read
  security-events: write

jobs:
  security:
    uses: zentto-erp/.github/.github/workflows/security.yml@main
    with:
      fail-on: critical   # critical | high | medium | none
    secrets: inherit
```

## Parámetros

| Input | Default | Descripción |
|---|---|---|
| `fail-on` | `critical` | Severidad que falla el build. Durante el cleanup del backlog: `critical`; una vez limpio: subir a `high`. |
| `semgrep-config` | (rulesets default) | Reglas custom si se necesitan. |
| `run-trivy` | `true` | Desactivar si el repo no tiene deps ni Dockerfile. |
| `run-gitleaks` | `true` | |
| `run-osv` | `true` | |
| `run-zizmor` | `true` | |
| `run-actionlint` | `true` | |
| `upload-sarif` | `true` | Subir SARIF a code scanning. En repos privados sin GHAS solo genera artifacts (no falla). |

## Outputs por ejecución

- **GitHub Step Summary** con resumen ejecutivo por herramienta.
- **Artifacts** con SARIF/JSON de cada scanner (retención 30 días).
- **Code scanning UI** (si `upload-sarif: true` y el repo lo soporta — gratis en públicos, requiere GHAS en privados).

## Plan de rollout (Abril 2026)

1. Merge de este workflow a `main` en `zentto-erp/.github` (vía PR desde `developer`).
2. En cada uno de los 32 repos de la org: PR añadiendo el caller workflow + `permissions: contents: read` en los workflows existentes (arregla 32 vulns de "Workflow does not contain permissions").
3. Correr el escaneo inicial, priorizar hallazgos:
   - **Críticos** (SSRF, command injection) → fix inmediato
   - **Altos** (rate limiting, ReDoS, CSRF, X-Frame-Options) → sprint por repo
   - **Medium** → backlog
4. Una vez limpio el backlog: subir `fail-on` a `high` para prevenir regresiones.
