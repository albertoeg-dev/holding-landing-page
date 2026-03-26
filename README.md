# Espejel Studio — Landing Page

Sitio web oficial de **Espejel Studio**, un estudio SaaS independiente fundado por Alberto Espejel. Construido con Vue 3 + Vite, diseñado para servir como presencia de negocio para procesadores de pago (Stripe) y como escaparate de los productos SaaS del estudio.

🌐 **Dominio:** [espejelstudio.dev](https://espejelstudio.dev)

---

## Stack

- **Vue 3** — Composition API
- **Vite** — bundler
- **Vue Router** — navegación con history mode
- **Nginx** — servidor en producción
- **Docker** — contenedor multi-stage (Node build → Nginx serve)
- **Google Cloud Run** — despliegue continuo desde repositorio

---

## Estructura

```
src/
├── components/
│   ├── NavBar.vue
│   ├── HeroSection.vue
│   ├── AboutSection.vue
│   ├── ProductsSection.vue
│   ├── TrustSection.vue
│   ├── ContactSection.vue
│   └── FooterSection.vue
├── views/
│   ├── HomeView.vue
│   ├── TermsView.vue
│   └── PrivacyView.vue
├── router/index.js
├── assets/
│   └── main.css
└── main.js
```

---

## Desarrollo local

```bash
npm install
npm run dev
```

## Build de producción

```bash
npm run build
```

## Docker (local)

```bash
docker build -t espejel-studio-landing .
docker run -p 8080:8080 espejel-studio-landing
```

---

## Despliegue

El despliegue se realiza automáticamente en **Google Cloud Run** mediante un trigger de Cloud Build conectado a este repositorio. Cada push a `main` dispara una nueva revisión.

---

## Contacto

**Alberto Espejel** — [alberto@espejelstudio.dev](mailto:alberto@espejelstudio.dev)
