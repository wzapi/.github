# 🚀 WZAPI

**WhatsApp Business API para GoHighLevel — Potencia tu negocio con mensajería inteligente.**

---

## 🎯 ¿Qué somos?

Una plataforma **SaaS multi-tenant** que reemplaza el canal de SMS en GoHighLevel por **WhatsApp + automatizaciones**. Procesamos millones de mensajes, gestionamos sesiones WhatsApp empresariales y nos integramos nativamente con GHL.

## 🧱 Arquitectura Modular

```
@wzapi/core          → Infraestructura compartida (DB, Redis, RabbitMQ)
@wzapi/auth          → Autenticación multi-tenant, MFA, roles
@wzapi/tenancy       → Cuentas, locations, memberships
@wzapi/billing       → Planes, suscripciones, créditos, Stripe
@wzapi/contacts      → Contact identity, CRM sync, consent
@wzapi/sessions      → Sesiones WhatsApp, QR, anti-ban
@wzapi/messaging     → Mensajería, inbox/outbox, deliveries
@wzapi/ghl           → Integración GoHighLevel (OAuth, webhooks)
@wzapi/settings      → Configuración por tenant
@wzapi/whitelabel    → Branding, dominios, temas
@wzapi/notifications → SMTP, webhooks, notificaciones
@wzapi/cache         → Cache distribuida
```

## 📦 Repositorios

| Repo | Propósito |
|------|-----------|
| [`core`](https://github.com/wzapi/core) | 🎯 Aplicación principal y orquestación |
| [`ui-kit`](https://github.com/wzapi/ui-kit) | 🎨 Biblioteca de componentes UI |
| [`gateway`](https://github.com/wzapi/gateway) | ⚙️ Gateway Go (whatsmeow) |
| `package_*` | 📦 Módulos independientes @wzapi/* |

## 🛠 Stack

```yaml
Backend:    Node.js 24 + TypeScript
Gateway:    Go + whatsmeow (fork)
Frontend:   React 19 + Next.js 16
Database:   PostgreSQL 17 (autoridad) + Redis (cache)
Broker:     RabbitMQ 4
UI:         shadcn/ui + Tailwind CSS 4
Infra:      Docker + GitHub Actions + 12 runners
```

## 🏗 Estado

````text
📋 Fase 0 — Constitución y especificación (GATE B)
🔧 Fase 1 — Developer Platform (en progreso...)
⚡ Fase 2+ — SaaS Core, Provider Contracts, WhatsApp Runtime
````

---

*Construido con ❤️ desde México*
