<script setup>
// No external dependencies needed
</script>

<template>
  <section class="hero">
    <!-- Background pattern -->
    <div class="hero__bg" aria-hidden="true">
      <div class="hero__bg-grid"></div>
      <div class="hero__bg-glow"></div>
    </div>

    <div class="container hero__inner">
      <div class="hero__badge fade-in">
        <span class="hero__badge-dot"></span>
        Estudio SaaS Independiente
      </div>

      <h1 class="hero__heading fade-in fade-in-delay-1">
        Productos SaaS simples.<br />
        <em class="hero__heading-em">Construidos para resolver</em><br />
        problemas reales.
      </h1>

      <p class="hero__subheading fade-in fade-in-delay-2">
        Espejel Studio desarrolla y opera una suite de herramientas de software enfocadas
        en resolver problemas prácticos con tecnología moderna e inteligencia artificial.
      </p>

      <div class="hero__actions fade-in fade-in-delay-3">
        <a href="#products" class="btn btn--primary hero__cta-main">
          Ver productos
          <svg width="14" height="14" viewBox="0 0 14 14" fill="none" aria-hidden="true">
            <path d="M2.5 7h9M8 3.5l3.5 3.5L8 10.5" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </a>
        <a href="#about" class="btn btn--outline">Saber más</a>
      </div>

      <div class="hero__meta fade-in fade-in-delay-4">
        <span class="hero__meta-item">
          <svg width="13" height="13" viewBox="0 0 13 13" fill="none" aria-hidden="true">
            <circle cx="6.5" cy="6.5" r="5.5" stroke="currentColor" stroke-width="1.3"/>
            <path d="M4 6.5l1.7 1.7L9 4.5" stroke="currentColor" stroke-width="1.3" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
          Pagos vía Stripe
        </span>
        <span class="hero__meta-divider" aria-hidden="true">·</span>
        <span class="hero__meta-item">
          <svg width="13" height="13" viewBox="0 0 13 13" fill="none" aria-hidden="true">
            <circle cx="6.5" cy="6.5" r="5.5" stroke="currentColor" stroke-width="1.3"/>
            <path d="M4 6.5l1.7 1.7L9 4.5" stroke="currentColor" stroke-width="1.3" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
          Independiente y autofinanciado
        </span>
        <span class="hero__meta-divider" aria-hidden="true">·</span>
        <span class="hero__meta-item">
          <svg width="13" height="13" viewBox="0 0 13 13" fill="none" aria-hidden="true">
            <circle cx="6.5" cy="6.5" r="5.5" stroke="currentColor" stroke-width="1.3"/>
            <path d="M4 6.5l1.7 1.7L9 4.5" stroke="currentColor" stroke-width="1.3" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
          Creado por Alberto Espejel
        </span>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  position: relative;
  padding: 96px 0 100px;
  border-bottom: 1px solid var(--color-gray-200);
  overflow: hidden;
}

/* Background effects */
.hero__bg {
  position: absolute;
  inset: 0;
  pointer-events: none;
}

.hero__bg-grid {
  position: absolute;
  inset: 0;
  background-image:
    linear-gradient(var(--color-gray-200) 1px, transparent 1px),
    linear-gradient(90deg, var(--color-gray-200) 1px, transparent 1px);
  background-size: 48px 48px;
  mask-image: radial-gradient(ellipse 80% 60% at 50% 0%, black 40%, transparent 100%);
  opacity: 0.5;
}

.hero__bg-glow {
  position: absolute;
  top: -120px;
  right: -80px;
  width: 500px;
  height: 500px;
  background: radial-gradient(circle, rgba(195, 235, 208, 0.35) 0%, transparent 70%);
  border-radius: 50%;
}

.hero__inner {
  position: relative;
  max-width: 760px;
}

.hero__badge {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  font-size: 12px;
  font-weight: 600;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: var(--color-gray-500);
  background-color: rgba(255,255,255,0.8);
  border: 1px solid var(--color-gray-200);
  padding: 6px 14px;
  border-radius: 100px;
  margin-bottom: 36px;
  backdrop-filter: blur(4px);
}

.hero__badge-dot {
  width: 6px;
  height: 6px;
  background-color: #6db88a;
  border-radius: 50%;
  flex-shrink: 0;
  box-shadow: 0 0 0 2px rgba(109, 184, 138, 0.25);
}

.hero__heading {
  font-size: clamp(38px, 6.5vw, 68px);
  font-weight: 800;
  letter-spacing: -0.035em;
  line-height: 1.07;
  color: var(--color-black);
  margin-bottom: 28px;
}

.hero__heading-em {
  font-style: normal;
  background: linear-gradient(135deg, #000 0%, #3a3a3a 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  position: relative;
}

.hero__heading-em::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: 2px;
  width: 100%;
  height: 3px;
  background: var(--color-accent);
  border-radius: 2px;
}

.hero__subheading {
  font-size: 18px;
  color: var(--color-gray-500);
  line-height: 1.7;
  max-width: 540px;
  margin-bottom: 44px;
  font-weight: 400;
}

.hero__actions {
  display: flex;
  align-items: center;
  gap: 12px;
  flex-wrap: wrap;
  margin-bottom: 52px;
}

.hero__cta-main {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  font-size: 15px;
  padding: 13px 22px;
  box-shadow: 0 1px 3px rgba(0,0,0,0.2), 0 4px 12px rgba(0,0,0,0.1);
}

.hero__cta-main:hover {
  gap: 12px;
}

.hero__actions .btn--outline {
  font-size: 15px;
  padding: 13px 22px;
}

.hero__meta {
  display: flex;
  align-items: center;
  gap: 16px;
  flex-wrap: wrap;
}

.hero__meta-item {
  display: flex;
  align-items: center;
  gap: 6px;
  font-size: 12.5px;
  color: var(--color-gray-400);
  font-weight: 500;
}

.hero__meta-divider {
  color: var(--color-gray-300);
  font-size: 12px;
}

@media (max-width: 600px) {
  .hero {
    padding: 72px 0 80px;
  }

  .hero__meta-divider {
    display: none;
  }

  .hero__meta {
    flex-direction: column;
    align-items: flex-start;
    gap: 8px;
  }

  .hero__bg-glow {
    width: 300px;
    height: 300px;
    top: -60px;
    right: -60px;
  }
}
</style>
