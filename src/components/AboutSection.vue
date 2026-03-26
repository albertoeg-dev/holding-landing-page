<script setup>
const values = [
  {
    label: 'Enfocado',
    description: 'Cada producto hace una cosa bien. Sin funciones innecesarias ni complejidad por el simple hecho de tenerla.',
  },
  {
    label: 'Transparente',
    description: 'Lo que ves es lo que obtienes. Precios, manejo de datos y modelo de negocio siempre claros.',
  },
  {
    label: 'Sostenible',
    description: 'Los productos están hechos para durar, se mantienen activamente y se diseñan pensando en clientes a largo plazo.',
  },
]
</script>

<template>
  <section id="about" class="section about-section">
    <div class="container">
      <div class="about__layout">
        <div class="about__content">
          <span class="section__label">Nosotros</span>
          <h2 class="section__heading">Un estudio construido para el largo plazo.</h2>
          <p class="about__body">
            Espejel Studio es un estudio SaaS independiente fundado por Alberto Espejel. El estudio se enfoca en
            construir y mantener productos de software pequeños y eficientes que resuelven problemas del mundo real.
            Cada producto está diseñado con simplicidad, rendimiento y usabilidad en mente.
          </p>
          <p class="about__body">
            En lugar de seguir tendencias, el estudio se concentra en puntos de dolor específicos — principalmente
            en e-commerce, productividad y datos — y lanza software que funciona de manera confiable desde el primer día.
          </p>
          <p class="about__founder">
            Fundado y operado por
            <strong>Alberto Espejel</strong>
            — desarrollador independiente y creador de productos.
          </p>
        </div>

        <div class="about__values">
          <div
            v-for="(value, i) in values"
            :key="value.label"
            class="about__value"
          >
            <div class="about__value-index">0{{ i + 1 }}</div>
            <div>
              <h3 class="about__value-label">{{ value.label }}</h3>
              <p class="about__value-desc">{{ value.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-section {
  background-color: var(--color-gray-50);
  border-top: 1px solid var(--color-gray-200);
  border-bottom: 1px solid var(--color-gray-200);
}

.about__layout {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 80px;
  align-items: start;
}

.about__content {
  max-width: 480px;
}

.about__body {
  font-size: 16px;
  color: var(--color-gray-500);
  line-height: 1.75;
  margin-bottom: 16px;
}

.about__body:last-of-type {
  margin-bottom: 24px;
}

.about__founder {
  font-size: 14px;
  color: var(--color-gray-400);
  padding-top: 20px;
  border-top: 1px solid var(--color-gray-200);
}

.about__founder strong {
  color: var(--color-gray-700);
  font-weight: 600;
}

.about__values {
  display: flex;
  flex-direction: column;
  gap: 32px;
}

.about__value {
  display: flex;
  gap: 20px;
  align-items: flex-start;
  padding: 20px;
  background: var(--color-white);
  border: 1px solid var(--color-gray-200);
  border-radius: var(--radius-md);
  transition: box-shadow 0.2s ease;
}

.about__value:hover {
  box-shadow: 0 4px 16px rgba(0,0,0,0.06);
}

.about__value-index {
  font-size: 11px;
  font-weight: 700;
  color: var(--color-gray-300);
  letter-spacing: 0.06em;
  min-width: 22px;
  padding-top: 3px;
}

.about__value-label {
  font-size: 15px;
  font-weight: 600;
  color: var(--color-black);
  margin-bottom: 6px;
}

.about__value-desc {
  font-size: 13.5px;
  color: var(--color-gray-500);
  line-height: 1.65;
}

@media (max-width: 860px) {
  .about__layout {
    grid-template-columns: 1fr;
    gap: 48px;
  }

  .about__content {
    max-width: 100%;
  }
}
</style>
