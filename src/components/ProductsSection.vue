<script setup>
const products = [
  {
    id: 'trackrseller',
    name: 'TrackrSeller',
    tagline: 'Analítica de ventas para vendedores en marketplaces.',
    description:
      'TrackrSeller se conecta a tus cuentas de vendedor en Amazon y Etsy para darte una vista limpia y unificada de tu negocio. Monitorea ingresos diarios, el rendimiento de cada listing, identifica patrones estacionales y recibe alertas cuando tus mejores productos empiezan a caer — todo desde un solo panel pensado para vendedores, no para analistas.',
    audience: 'Vendedores en Amazon y Etsy',
    url: 'https://trackrseller.espejelstudio.dev',
    tags: ['Analítica', 'E-commerce', 'Marketplaces'],
  },
  {
    id: 'contentforge',
    name: 'ContentForge',
    tagline: 'Copy de producto con IA para tiendas en línea.',
    description:
      'ContentForge usa IA entrenada en copy de e-commerce de alta conversión para generar títulos, bullets, descripciones y anuncios para cualquier producto — en segundos. Tengas diez listings o diez mil, mantiene una voz de marca consistente mientras apunta a las palabras clave correctas para SEO y búsqueda pagada.',
    audience: 'Marcas y agencias de e-commerce',
    url: 'https://contentforge.espejelstudio.dev',
    tags: ['IA', 'Copywriting', 'SEO'],
  },
  {
    id: 'pricewatch',
    name: 'PriceWatch',
    tagline: 'Monitoreo automatizado de precios de competidores.',
    description:
      'PriceWatch monitorea los precios de productos de la competencia en los principales sitios de retail y te avisa cuando cambian. Define umbrales personalizados, rastrea tendencias históricas de precios y mantente competitivo sin revisar sitios manualmente. Diseñado para retailers en línea que necesitan reaccionar rápido a los movimientos del mercado.',
    audience: 'Retailers en línea y brand managers',
    url: 'https://pricewatch.espejelstudio.dev',
    tags: ['Monitoreo', 'Retail', 'Automatización'],
  },
]
</script>

<template>
  <section id="products" class="section">
    <div class="container">
      <div class="products__header">
        <span class="section__label">Productos</span>
        <h2 class="section__heading">Software que resuelve problemas específicos.</h2>
        <p class="section__subheading">
          Cada producto tiene su propio alcance, precio y mantenimiento. Sin paquetes ni ventas cruzadas —
          solo herramientas que hacen lo que prometen.
        </p>
      </div>

      <div class="products__grid">
        <article
          v-for="product in products"
          :key="product.id"
          class="product-card"
        >
          <div class="product-card__header">
            <div class="product-card__icon" :data-id="product.id" aria-hidden="true">
              {{ product.name.charAt(0) }}
            </div>
            <div class="product-card__tags">
              <span
                v-for="tag in product.tags"
                :key="tag"
                class="product-card__tag"
              >{{ tag }}</span>
            </div>
          </div>

          <h3 class="product-card__name">{{ product.name }}</h3>
          <p class="product-card__tagline">{{ product.tagline }}</p>
          <p class="product-card__description">{{ product.description }}</p>

          <div class="product-card__footer">
            <span class="product-card__audience">
              <svg width="13" height="13" viewBox="0 0 13 13" fill="none" aria-hidden="true">
                <circle cx="6.5" cy="4.5" r="2.5" stroke="currentColor" stroke-width="1.3"/>
                <path d="M1.5 11c0-2.21 2.239-4 5-4s5 1.79 5 4" stroke="currentColor" stroke-width="1.3" stroke-linecap="round"/>
              </svg>
              {{ product.audience }}
            </span>
            <a
              :href="product.url"
              target="_blank"
              rel="noopener noreferrer"
              class="product-card__link"
            >
              Ver más
              <svg width="13" height="13" viewBox="0 0 13 13" fill="none" aria-hidden="true">
                <path d="M2.5 6.5h8M7 3.5l3 3-3 3" stroke="currentColor" stroke-width="1.4" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
            </a>
          </div>
        </article>
      </div>
    </div>
  </section>
</template>

<style scoped>
.products__header {
  max-width: 600px;
  margin-bottom: 56px;
}

.products__grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}

.product-card {
  display: flex;
  flex-direction: column;
  background-color: var(--color-white);
  border: 1px solid var(--color-gray-200);
  border-radius: var(--radius-lg);
  padding: 28px;
  position: relative;
  overflow: hidden;
  transition: border-color 0.2s ease, box-shadow 0.2s ease, transform 0.2s ease;
}

.product-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 3px;
  background: linear-gradient(90deg, var(--color-black) 0%, #c3ebd0 100%);
  border-radius: var(--radius-lg) var(--radius-lg) 0 0;
  opacity: 0;
  transition: opacity 0.25s ease;
}

.product-card:hover {
  border-color: var(--color-gray-300);
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.09);
  transform: translateY(-3px);
}

.product-card:hover::before {
  opacity: 1;
}

.product-card__header {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  margin-bottom: 20px;
}

.product-card__icon {
  width: 44px;
  height: 44px;
  border-radius: var(--radius-md);
  background: linear-gradient(135deg, #111 0%, #333 100%);
  color: var(--color-white);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 17px;
  font-weight: 700;
  flex-shrink: 0;
  box-shadow: 0 2px 8px rgba(0,0,0,0.2);
}

.product-card__icon[data-id="contentforge"] {
  background: linear-gradient(135deg, #1a1a2e 0%, #2d2d4e 100%);
}

.product-card__icon[data-id="pricewatch"] {
  background: linear-gradient(135deg, #111827 0%, #1f2937 100%);
}

.product-card__tags {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
  justify-content: flex-end;
}

.product-card__tag {
  font-size: 11px;
  font-weight: 500;
  color: var(--color-gray-500);
  background-color: var(--color-gray-100);
  padding: 3px 9px;
  border-radius: 100px;
  letter-spacing: 0.02em;
}

.product-card__name {
  font-size: 18px;
  font-weight: 700;
  color: var(--color-black);
  letter-spacing: -0.02em;
  margin-bottom: 4px;
}

.product-card__tagline {
  font-size: 14px;
  font-weight: 500;
  color: var(--color-gray-400);
  margin-bottom: 16px;
}

.product-card__description {
  font-size: 14px;
  color: var(--color-gray-500);
  line-height: 1.7;
  flex: 1;
  margin-bottom: 24px;
}

.product-card__footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-top: 20px;
  border-top: 1px solid var(--color-gray-100);
}

.product-card__audience {
  display: flex;
  align-items: center;
  gap: 6px;
  font-size: 12px;
  color: var(--color-gray-400);
  font-weight: 500;
}

.product-card__link {
  display: flex;
  align-items: center;
  gap: 5px;
  font-size: 13px;
  font-weight: 600;
  color: var(--color-black);
  transition: gap 0.15s ease;
}

.product-card__link:hover {
  gap: 8px;
}

@media (max-width: 960px) {
  .products__grid {
    grid-template-columns: 1fr 1fr;
  }
}

@media (max-width: 600px) {
  .products__grid {
    grid-template-columns: 1fr;
  }
}
</style>
