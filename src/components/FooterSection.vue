<script setup>
import { RouterLink } from 'vue-router'

const currentYear = new Date().getFullYear()
</script>

<template>
  <footer class="footer">
    <div class="container footer__inner">
      <div class="footer__brand">
        <div class="footer__logo">
          <span class="footer__logo-mark">ES</span>
          <span class="footer__logo-text">Espejel Studio</span>
        </div>
        <p class="footer__tagline">
          Estudio SaaS independiente.<br />
          Construido y operado por Alberto Espejel.
        </p>
        <a href="mailto:alberto@espejelstudio.dev" class="footer__email">
          alberto@espejelstudio.dev
        </a>
      </div>

      <nav class="footer__nav" aria-label="Footer navigation">
        <div class="footer__nav-group">
          <p class="footer__nav-label">Productos</p>
          <a href="https://trackrseller.espejelstudio.dev" target="_blank" rel="noopener noreferrer" class="footer__nav-link">TrackrSeller</a>
          <a href="https://contentforge.espejelstudio.dev" target="_blank" rel="noopener noreferrer" class="footer__nav-link">ContentForge</a>
          <a href="https://pricewatch.espejelstudio.dev" target="_blank" rel="noopener noreferrer" class="footer__nav-link">PriceWatch</a>
        </div>

        <div class="footer__nav-group">
          <p class="footer__nav-label">Empresa</p>
          <a href="#about" class="footer__nav-link">Nosotros</a>
          <a href="#contact" class="footer__nav-link">Contacto</a>
          <a href="#products" class="footer__nav-link">Todos los productos</a>
        </div>

        <div class="footer__nav-group">
          <p class="footer__nav-label">Legal</p>
          <RouterLink to="/terms" class="footer__nav-link">Términos y condiciones</RouterLink>
          <RouterLink to="/privacy" class="footer__nav-link">Política de privacidad</RouterLink>
        </div>
      </nav>
    </div>

    <div class="container footer__bottom">
      <p class="footer__copy">
        &copy; {{ currentYear }} Espejel Studio. All rights reserved.
      </p>
      <p class="footer__copy footer__copy--right">
        Pagos procesados por <strong>Stripe</strong>
      </p>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background-color: #0a0a0a;
  border-top: 1px solid rgba(255,255,255,0.06);
  margin-top: auto;
}

.footer__inner {
  display: grid;
  grid-template-columns: 1.5fr 2fr;
  gap: 80px;
  padding-top: 56px;
  padding-bottom: 48px;
}

.footer__brand {
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.footer__logo {
  display: flex;
  align-items: center;
  gap: 10px;
  font-weight: 700;
  font-size: 15px;
  color: #ffffff;
  letter-spacing: -0.01em;
  margin-bottom: 4px;
}

.footer__logo-mark {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 28px;
  height: 28px;
  background-color: #ffffff;
  color: #000000;
  font-size: 10px;
  font-weight: 700;
  letter-spacing: 0.04em;
  border-radius: var(--radius-sm);
  flex-shrink: 0;
}

.footer__tagline {
  font-size: 14px;
  color: rgba(255,255,255,0.4);
  line-height: 1.65;
}

.footer__email {
  font-size: 13px;
  font-weight: 500;
  color: rgba(255,255,255,0.4);
  transition: color 0.15s;
}

.footer__email:hover {
  color: rgba(255,255,255,0.8);
}

.footer__nav {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}

.footer__nav-group {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.footer__nav-label {
  font-size: 11px;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  color: rgba(255,255,255,0.25);
  margin-bottom: 4px;
}

.footer__nav-link {
  font-size: 14px;
  color: rgba(255,255,255,0.45);
  transition: color 0.15s;
}

.footer__nav-link:hover {
  color: rgba(255,255,255,0.9);
}

.footer__bottom {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-top: 20px;
  padding-bottom: 24px;
  border-top: 1px solid rgba(255,255,255,0.07);
  flex-wrap: wrap;
  gap: 8px;
}

.footer__copy {
  font-size: 13px;
  color: rgba(255,255,255,0.25);
}

.footer__copy strong {
  font-weight: 600;
  color: rgba(255,255,255,0.4);
}

@media (max-width: 860px) {
  .footer__inner {
    grid-template-columns: 1fr;
    gap: 40px;
  }
}

@media (max-width: 480px) {
  .footer__nav {
    grid-template-columns: 1fr 1fr;
  }

  .footer__bottom {
    flex-direction: column;
    align-items: flex-start;
  }
}
</style>
