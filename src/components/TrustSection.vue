<script setup>
const items = [
  {
    heading: 'Operado por Espejel Studio',
    body: 'Todos los productos listados en este sitio son desarrollados y operados por Espejel Studio, un negocio de software independiente fundado y dirigido por Alberto Espejel.',
  },
  {
    heading: 'Pagos vía Stripe',
    body: 'Toda la facturación se maneja de forma segura a través de Stripe, un procesador de pagos de confianza mundial. Los datos de tu tarjeta nunca se almacenan en nuestros servidores.',
  },
  {
    heading: 'Alcance de producto claro',
    body: 'Cada producto tiene su propia página de precios, lista de funciones y documentación. Siempre sabrás exactamente por qué estás pagando antes de suscribirte.',
  },
  {
    heading: 'Preguntas de facturación y disputas',
    body: 'Si tienes dudas sobre un cargo, necesitas cancelar o quieres un reembolso, contacta directamente a alberto@espejelstudio.dev y lo resolveremos de inmediato.',
  },
]
</script>

<template>
  <section class="section trust">
    <div class="container">
      <div class="trust__header">
        <span class="section__label">Transparencia</span>
        <h2 class="section__heading">Cómo funciona este negocio.</h2>
        <p class="section__subheading">
          Creemos que los clientes deben entender completamente qué están comprando y a quién le están comprando.
        </p>
      </div>

      <div class="trust__grid">
        <div
          v-for="item in items"
          :key="item.heading"
          class="trust__item"
        >
          <div class="trust__dot" aria-hidden="true"></div>
          <div>
            <h3 class="trust__item-heading">{{ item.heading }}</h3>
            <p class="trust__item-body">{{ item.body }}</p>
          </div>
        </div>
      </div>

      <div class="trust__stripe">
        <div class="trust__stripe-inner">
          <p class="trust__stripe-label">Procesador de pagos</p>
          <p class="trust__stripe-value">Stripe, Inc. — PCI DSS Nivel 1 certificado</p>
        </div>
        <div class="trust__stripe-inner">
          <p class="trust__stripe-label">Operador del negocio</p>
          <p class="trust__stripe-value">Alberto Espejel — Espejel Studio</p>
        </div>
        <div class="trust__stripe-inner">
          <p class="trust__stripe-label">Correo de soporte</p>
          <a href="mailto:alberto@espejelstudio.dev" class="trust__stripe-link">
            alberto@espejelstudio.dev
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.trust {
  background: linear-gradient(180deg, #fafafa 0%, #f0f0f0 100%);
  border-top: 1px solid var(--color-gray-200);
}

.trust__header {
  max-width: 600px;
  margin-bottom: 56px;
}

.trust__grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 32px;
  margin-bottom: 48px;
}

.trust__item {
  display: flex;
  gap: 16px;
  align-items: flex-start;
}

.trust__dot {
  width: 8px;
  height: 8px;
  background-color: #6db88a;
  border-radius: 50%;
  flex-shrink: 0;
  margin-top: 7px;
  box-shadow: 0 0 0 3px rgba(109, 184, 138, 0.2);
}

.trust__item-heading {
  font-size: 15px;
  font-weight: 600;
  color: var(--color-black);
  margin-bottom: 6px;
}

.trust__item-body {
  font-size: 14px;
  color: var(--color-gray-500);
  line-height: 1.7;
}

.trust__stripe {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 0;
  border: 1px solid var(--color-gray-200);
  border-radius: var(--radius-lg);
  overflow: hidden;
  background-color: var(--color-white);
}

.trust__stripe-inner {
  padding: 20px 24px;
  border-right: 1px solid var(--color-gray-200);
}

.trust__stripe-inner:last-child {
  border-right: none;
}

.trust__stripe-label {
  font-size: 11px;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.07em;
  color: var(--color-gray-400);
  margin-bottom: 6px;
}

.trust__stripe-value {
  font-size: 14px;
  font-weight: 500;
  color: var(--color-gray-700);
}

.trust__stripe-link {
  font-size: 14px;
  font-weight: 500;
  color: var(--color-black);
  text-decoration: underline;
  text-underline-offset: 3px;
  transition: opacity 0.15s;
}

.trust__stripe-link:hover {
  opacity: 0.65;
}

@media (max-width: 860px) {
  .trust__grid {
    grid-template-columns: 1fr;
    gap: 24px;
  }

  .trust__stripe {
    grid-template-columns: 1fr;
  }

  .trust__stripe-inner {
    border-right: none;
    border-bottom: 1px solid var(--color-gray-200);
  }

  .trust__stripe-inner:last-child {
    border-bottom: none;
  }
}
</style>
