<div align="center">

# Zentto ERP

**Plataforma empresarial modular para LATAM**

ERP · POS · Contabilidad · Nómina · Inventario · Hotel · Medical · Tickets · Rental · Education · Marketplace

[![Website](https://img.shields.io/badge/zentto.net-0ea5e9?style=for-the-badge&logo=globe&logoColor=white)](https://zentto.net)
[![Docs](https://img.shields.io/badge/docs.zentto.net-22c55e?style=for-the-badge&logo=readthedocs&logoColor=white)](https://docs.zentto.net)
[![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org)
[![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)](https://nextjs.org)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)](https://postgresql.org)
[![.NET](https://img.shields.io/badge/.NET_9-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)](https://dotnet.microsoft.com)

</div>

---

## ¿Qué es Zentto?

**Zentto** es un ecosistema SaaS multi-tenant de aplicaciones empresariales para LATAM (Venezuela, España, Colombia, México y Estados Unidos). Combina un ERP completo con verticales especializadas (hotelería, salud, ticketing, alquiler, educación, inmobiliaria) y herramientas de soporte (notificaciones, reportes, agente fiscal, datagrid, observabilidad).

Todas las aplicaciones comparten **infraestructura de autenticación, notificaciones, observabilidad y diseño**, pero pueden desplegarse de forma independiente.

---

## 🧩 Productos

### Core ERP

| Producto | Repo | Descripción |
|----------|------|-------------|
| **Zentto ERP** | [zentto-web](https://github.com/zentto-erp/zentto-web) | Core: facturación, POS, contabilidad, inventario, nómina, ecommerce |
| **Zentto Auth** | [zentto-auth](https://github.com/zentto-erp/zentto-auth) | Microservicio centralizado de autenticación (cookies HttpOnly) |
| **Zentto Notify** | [zentto-notify](https://github.com/zentto-erp/zentto-notify) | Notificaciones multi-canal: email, SMS, push, OTP, WhatsApp |
| **Zentto Cache** | [zentto-cache](https://github.com/zentto-erp/zentto-cache) | Servicio de cache compartido |
| **Zentto Obs** | [zentto-obs](https://github.com/zentto-erp/zentto-obs) | SDK de observabilidad (Kafka + Elasticsearch + Kibana) |
| **Zentto Infra** | [zentto-infra](https://github.com/zentto-erp/zentto-infra) | IaC, Docker, Nginx, CI/CD del servidor de producción |

### Verticales especializadas

| Producto | Repo | Descripción |
|----------|------|-------------|
| **Zentto Hotel** | [zentto-hotel](https://github.com/zentto-erp/zentto-hotel) | PMS hotelero: reservas, housekeeping, tarifas, canales |
| **Zentto Medical** | [zentto-medical](https://github.com/zentto-erp/zentto-medical) | Plataforma médica: citas, pacientes, recetas, hospitalización |
| **Zentto Tickets** | [zentto-tickets](https://github.com/zentto-erp/zentto-tickets) | Ticketing y eventos con mapas de asientos |
| **Zentto Rental** | [zentto-rental](https://github.com/zentto-erp/zentto-rental) | Renta de vehículos (ACRISS, fleet, inspecciones) |
| **Zentto Education** | [zentto-education](https://github.com/zentto-erp/zentto-education) | Sistema de información estudiantil (SIS) |
| **Zentto Inmobiliario** | [zentto-inmobiliario](https://github.com/zentto-erp/zentto-inmobiliario) | Gestión inmobiliaria avanzada |
| **Zentto Broker** | [zentto-broker](https://github.com/zentto-erp/zentto-broker) | Marketplace y pagos B2B |

### Herramientas y librerías

| Producto | Repo | Descripción | NPM |
|----------|------|-------------|-----|
| **ZenttoDataGrid** | [zentto-datagrid](https://github.com/zentto-erp/zentto-datagrid) | DataGrid web component, alternativa libre a AG Grid Enterprise | [![npm](https://img.shields.io/npm/v/@zentto/datagrid)](https://www.npmjs.com/package/@zentto/datagrid) |
| **Zentto Studio** | [zentto-studio](https://github.com/zentto-erp/zentto-studio) | Runtime UI builder — genera apps desde JSON |
| **Zentto Report Engine** | [zentto-report](https://github.com/zentto-erp/zentto-report) | Alternativa web a Crystal Reports |
| **Zentto Report Studio** | [zentto-report-studio](https://github.com/zentto-erp/zentto-report-studio) | Editor de reportes Electron |
| **Zentto Sites** | [zentto-sites](https://github.com/zentto-erp/zentto-sites) | API para crear y publicar landings estáticas |
| **Zentto Landing Designer** | [zentto-landing-designer](https://github.com/zentto-erp/zentto-landing-designer) | Visual builder para landing pages |
| **Zentto CLI** | [zentto-cli](https://github.com/zentto-erp/zentto-cli) | CLI para crear, build y deploy de landings |

### Móvil y desktop

| Producto | Repo | Descripción |
|----------|------|-------------|
| **Zentto Mobile** | [zentto-mobile](https://github.com/zentto-erp/zentto-mobile) | App móvil principal (React Native + Expo) |
| **Zentto Mobile Panel** | [zentto-mobile-panel](https://github.com/zentto-erp/zentto-mobile-panel) | Wrapper Capacitor del panel admin |
| **Zentto Tauri Panel** | [zentto-tauri-panel](https://github.com/zentto-erp/zentto-tauri-panel) | App de escritorio Tauri v2 (Rust, ~3 MB) |

### Hardware fiscal y agentes

| Producto | Repo | Descripción |
|----------|------|-------------|
| **Zentto Fiscal Agent** | [zentto-fiscal-agent](https://github.com/zentto-erp/zentto-fiscal-agent) | Servicio Windows .NET 9 para impresoras fiscales |
| **Releases públicas** | [zentto-fiscal-agent-releases](https://github.com/zentto-erp/zentto-fiscal-agent-releases) | Instaladores firmados del Fiscal Agent |
| **Copilot Agents** | [zentto-erp/copilot-agents](https://github.com/zentto-erp/copilot-agents) | Agentes de IA para automatización interna |

### Documentación y soporte

| Recurso | Repo | URL |
|---------|------|-----|
| **Landing pública** | [zentto-docs](https://github.com/zentto-erp/zentto-docs) | [zentto.net](https://zentto.net) |
| **Manual del ERP** | [zentto-erp-docs](https://github.com/zentto-erp/zentto-erp-docs) | [docs.zentto.net](https://docs.zentto.net) |
| **Soporte y bugs** | [zentto-support](https://github.com/zentto-erp/zentto-support) | [Reportar issue](https://github.com/zentto-erp/zentto-support/issues) |

---

## 🛠 Stack Tecnológico

```
Backend           →  Node.js · Express · TypeScript · Zod
Frontend          →  Next.js 16 · React 19 · MUI 7 · TanStack Query
Bases de datos    →  PostgreSQL 16 + SQL Server 2019 (dual-engine)
Migraciones       →  Goose (SQL Server compat 110)
Móvil             →  React Native · Expo · Capacitor · Tauri
Fiscal Agent      →  .NET 9 Windows Service
Notificaciones    →  Node.js · Redis · Nodemailer · DKIM · WhatsApp Cloud API
Infra             →  Hetzner CX33 · Docker · Nginx · GitHub Actions · ghcr.io
DNS / CDN         →  Cloudflare (proxied)
Observabilidad    →  Kafka · Elasticsearch · Kibana · APM
Pagos             →  Paddle · Stripe (próximo)
```

---

## 🌐 Producción

| Componente | URL |
|------------|-----|
| Landing | [zentto.net](https://zentto.net) |
| Documentación | [docs.zentto.net](https://docs.zentto.net) |
| ERP Frontend | [app.zentto.net](https://app.zentto.net) |
| ERP API | [api.zentto.net](https://api.zentto.net) |
| Notificaciones | [notify.zentto.net](https://notify.zentto.net) |
| Hotel | [hotel.zentto.net](https://hotel.zentto.net) |
| Medical | [medical.zentto.net](https://medical.zentto.net) |
| Tickets | [tickets.zentto.net](https://tickets.zentto.net) |
| Rental | [rental.zentto.net](https://rental.zentto.net) |
| Broker | [broker.zentto.net](https://broker.zentto.net) |
| Vault | [vault.zentto.net](https://vault.zentto.net) |

Multi-tenant: cada cliente recibe un subdominio propio bajo `*.zentto.net` con su base de datos aislada.

---

## 🔒 Seguridad

Toda la organización sigue el [Estándar de Seguridad Zentto](https://github.com/zentto-erp/zentto-infra/blob/main/docs/security-standards.md):

- **Cookies HttpOnly** — nunca tokens en `localStorage` ni cabeceras `Authorization` desde el browser.
- **Auth centralizado** vía [@zentto/auth-client](https://github.com/zentto-erp/zentto-auth).
- **Rate limiting** y **CORS** con `credentials: true` por dominio.
- **Sanitización PII** automática en todos los logs.
- **Docker non-root**, contenedores con healthchecks y resource limits.
- **Secretos** en Vaultwarden self-hosted ([vault.zentto.net](https://vault.zentto.net)).

---

## 📣 Contacto

- 🌍 Web: [zentto.net](https://zentto.net)
- 📧 Email: [info@zentto.net](mailto:info@zentto.net)
- 📚 Docs: [docs.zentto.net](https://docs.zentto.net)
- 🐛 Bugs y soporte: [zentto-support/issues](https://github.com/zentto-erp/zentto-support/issues)

---

<div align="center">

Hecho con ❤️ para empresas de LATAM · © Zentto

</div>
