<div align="center">

# Zentto ERP

**Plataforma empresarial modular para LATAM**

Facturación · POS · Contabilidad · Nómina · Inventario · Ecommerce · Notificaciones

[![Website](https://img.shields.io/badge/zentto.net-0ea5e9?style=for-the-badge&logo=globe&logoColor=white)](https://zentto.net)
[![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)](https://nodejs.org)
[![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)](https://nextjs.org)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)](https://postgresql.org)
[![.NET](https://img.shields.io/badge/.NET_9-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)](https://dotnet.microsoft.com)

</div>

---

## ¿Qué es Zentto?

Zentto es un ERP SaaS multi-tenant diseñado para empresas en Venezuela, España, Colombia y México. Cubre el ciclo completo de negocio desde el punto de venta hasta la contabilidad, con soporte para impresoras fiscales y periféricos locales.

## Módulos

| Módulo | Descripción |
|--------|-------------|
| **POS** | Punto de venta con soporte fiscal (PNP, Rigaza, HKA) |
| **Ventas** | Facturación, cotizaciones y cuentas por cobrar |
| **Contabilidad** | Mayor general, balances, ajuste por inflación COLGAAP/VEN-NIF |
| **Inventario** | Control de stock, movimientos y valuación |
| **Nómina** | Cálculo de nómina Venezuela (IVSS, FAOV, LPH) |
| **Ecommerce** | Tienda online integrada con inventario |
| **Notificaciones** | Email, SMS, Push, OTP multi-canal |
| **Restaurante** | Mesas, comandas y cocina en tiempo real |

## Repositorios

| Repo | Descripción | Visibilidad |
|------|-------------|-------------|
| [zentto-web](https://github.com/zentto-erp/zentto-web) | Core ERP: API Node.js + Frontend Next.js | Privado |
| [zentto-notify](https://github.com/zentto-erp/zentto-notify) | Microservicio de notificaciones multi-canal | Privado |
| [zentto-fiscal-agent](https://github.com/zentto-erp/zentto-fiscal-agent) | Agente fiscal Windows (.NET 9) | Privado |
| [zentto-fiscal-agent-releases](https://github.com/zentto-erp/zentto-fiscal-agent-releases) | Releases públicas del instalador | **Público** |
| [zentto-broker](https://github.com/zentto-erp/zentto-broker) | Marketplace y pagos B2B | Privado |
| [zentto-docs](https://github.com/zentto-erp/zentto-docs) | Landing page y documentación (Astro) | Privado |
| [zentto-infra](https://github.com/zentto-erp/zentto-infra) | IaC, Docker, Nginx, CI/CD | Privado |

## Stack Tecnológico

```
Backend          →  Node.js + Express + TypeScript
Frontend         →  Next.js 14 (App Router) + MUI + Zustand
Base de datos    →  PostgreSQL 16 + SQL Server (dual-engine)
Fiscal Agent     →  .NET 9 Windows Service
Notificaciones   →  Node.js + Redis + Nodemailer + DKIM
Infra            →  Hetzner CX33 · Docker · Nginx · GitHub Actions
DNS/CDN          →  Cloudflare
```

## Producción

| Componente | URL |
|------------|-----|
| ERP App | [app.zentto.net](https://app.zentto.net) |
| API | [api.zentto.net](https://api.zentto.net) |
| Docs | [zentto.net](https://zentto.net) |
| Notificaciones | [notify.zentto.net](https://notify.zentto.net) |

---

<div align="center">

Hecho con ❤️ para empresas de LATAM · [zentto.net](https://zentto.net) · [info@zentto.net](mailto:info@zentto.net)

</div>
