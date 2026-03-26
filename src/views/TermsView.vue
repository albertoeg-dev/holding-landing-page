<script setup>
const lastUpdated = '26 de marzo de 2026'
</script>

<template>
  <main class="legal-page">
    <div class="container legal-page__container">
      <div class="legal-page__header">
        <RouterLink to="/" class="legal-page__back">
          <svg width="14" height="14" viewBox="0 0 14 14" fill="none" aria-hidden="true">
            <path d="M9 2L4 7l5 5" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
          Volver al inicio
        </RouterLink>
        <h1 class="legal-page__title">Términos y Condiciones</h1>
        <p class="legal-page__meta">Espejel Studio · Última actualización: {{ lastUpdated }}</p>
      </div>

      <div class="legal-page__body">

        <section class="legal-section">
          <h2>1. Acerca de estos términos</h2>
          <p>
            Estos Términos y Condiciones rigen el uso de todos los productos y servicios de software ofrecidos por
            Espejel Studio ("nosotros" o "el Estudio"), un negocio de software independiente operado por Alberto
            Espejel bajo el dominio espejelstudio.dev.
          </p>
          <p>
            Al acceder o utilizar cualquier producto operado por Espejel Studio, aceptas quedar vinculado por estos
            términos. Si no estás de acuerdo, no utilices nuestros servicios.
          </p>
        </section>

        <section class="legal-section">
          <h2>2. Descripción de los servicios</h2>
          <p>
            Espejel Studio desarrolla, opera y mantiene una colección de productos SaaS (Software como Servicio)
            independientes. Cada producto es una herramienta de software basada en web diseñada para resolver
            problemas específicos de negocio o productividad. Los productos actuales incluyen, entre otros:
          </p>
          <ul>
            <li><strong>TrackrSeller</strong> — Panel de analítica de ventas para vendedores en marketplaces (Amazon, Etsy).</li>
            <li><strong>ContentForge</strong> — Generador de copy de producto con IA para e-commerce.</li>
            <li><strong>PriceWatch</strong> — Monitoreo automatizado de precios de competidores para retailers en línea.</li>
          </ul>
          <p>
            Cada producto puede tener sus propios términos específicos, estructura de precios y conjunto de funciones,
            los cuales se documentan claramente en el sitio web o aplicación de ese producto.
          </p>
        </section>

        <section class="legal-section">
          <h2>3. Registro de cuenta</h2>
          <p>
            Para utilizar la mayoría de nuestros productos necesitarás crear una cuenta. Aceptas proporcionar
            información precisa, actual y completa al registrarte, y mantener confidenciales tus credenciales de acceso.
            Eres responsable de toda la actividad que ocurra bajo tu cuenta.
          </p>
          <p>
            Debes notificarnos de inmediato a alberto@espejelstudio.dev si sospechas un acceso no autorizado a tu cuenta.
          </p>
        </section>

        <section class="legal-section">
          <h2>4. Pagos y facturación</h2>
          <p>
            Todos los pagos se procesan de forma segura a través de <strong>Stripe, Inc.</strong>, un procesador de
            pagos externo. Espejel Studio no almacena los datos de tu tarjeta de crédito en sus servidores.
          </p>
          <p>
            Las cuotas de suscripción se cobran por adelantado de forma recurrente (mensual o anual, según el plan
            que elijas). Al proporcionar información de pago, nos autorizas a cobrar tu método de pago por todas las
            tarifas asociadas a tu suscripción.
          </p>
          <p>
            Los precios pueden cambiar ocasionalmente. Notificaremos con al menos 30 días de anticipación cualquier
            cambio de precio para los suscriptores existentes.
          </p>
          <p>
            Si un cargo en tu estado de cuenta aparece como "Espejel Studio" o "ES Studio", proviene de uno de
            nuestros productos SaaS. Para cualquier duda o disputa de facturación, contáctanos en alberto@espejelstudio.dev.
          </p>
        </section>

        <section class="legal-section">
          <h2>5. Política de reembolsos</h2>
          <p>
            Si no estás satisfecho con un producto, puedes solicitar un reembolso dentro de los <strong>14 días</strong>
            posteriores a tu compra inicial o renovación, contactando a alberto@espejelstudio.dev. Las solicitudes de
            reembolso se evalúan caso por caso. Estamos comprometidos a resolver cualquier problema de manera justa y oportuna.
          </p>
          <p>
            No ofrecemos reembolsos por períodos de suscripción parciales después de la ventana de 14 días, excepto
            cuando lo exija la ley aplicable.
          </p>
        </section>

        <section class="legal-section">
          <h2>6. Cancelación</h2>
          <p>
            Puedes cancelar tu suscripción en cualquier momento desde la configuración de tu cuenta. La cancelación
            surte efecto al final de tu período de facturación actual; seguirás teniendo acceso al producto hasta
            entonces. No cobramos tarifas de cancelación.
          </p>
        </section>

        <section class="legal-section">
          <h2>7. Uso aceptable</h2>
          <p>Aceptas no usar nuestros productos para:</p>
          <ul>
            <li>Violar leyes o regulaciones aplicables.</li>
            <li>Hacer scraping, ingeniería inversa o reproducir cualquier parte de nuestros servicios sin permiso escrito.</li>
            <li>Intentar obtener acceso no autorizado a nuestros sistemas o cuentas de otros usuarios.</li>
            <li>Transmitir contenido dañino, ofensivo o ilegal.</li>
            <li>Usar los servicios para competir o replicar los productos de Espejel Studio.</li>
          </ul>
          <p>
            Nos reservamos el derecho de suspender o cancelar el acceso por violaciones a estos términos.
          </p>
        </section>

        <section class="legal-section">
          <h2>8. Propiedad intelectual</h2>
          <p>
            Todo el software, código, diseños, marcas comerciales y contenido dentro de los productos de Espejel Studio
            son propiedad exclusiva de Alberto Espejel / Espejel Studio. Nada en estos términos te otorga derechos
            sobre nuestra propiedad intelectual más allá de una licencia limitada y no exclusiva para usar los productos
            según su propósito.
          </p>
        </section>

        <section class="legal-section">
          <h2>9. Disponibilidad y tiempo de actividad</h2>
          <p>
            Buscamos mantener una alta disponibilidad en todos los productos, pero no garantizamos acceso ininterrumpido.
            Los servicios pueden estar temporalmente no disponibles por mantenimiento, actualizaciones o circunstancias
            fuera de nuestro control. Comunicaremos los tiempos de inactividad planificados con anticipación cuando sea posible.
          </p>
        </section>

        <section class="legal-section">
          <h2>10. Limitación de responsabilidad</h2>
          <p>
            En la máxima medida permitida por la ley aplicable, Espejel Studio y Alberto Espejel no serán responsables
            por daños indirectos, incidentales, especiales, consecuentes o punitivos derivados del uso de nuestros
            productos, incluso si se advirtió sobre la posibilidad de tales daños.
          </p>
          <p>
            Nuestra responsabilidad total hacia ti por cualquier reclamación derivada de estos términos no excederá el
            monto que nos hayas pagado en los tres meses previos a la reclamación.
          </p>
        </section>

        <section class="legal-section">
          <h2>11. Legislación aplicable</h2>
          <p>
            Estos términos se rigen e interpretan de acuerdo con la legislación aplicable. Cualquier disputa se resolverá
            mediante negociación de buena fe antes de recurrir a procedimientos legales formales.
          </p>
        </section>

        <section class="legal-section">
          <h2>12. Cambios a estos términos</h2>
          <p>
            Podemos actualizar estos términos periódicamente. Si los cambios son sustanciales, te notificaremos por correo
            electrónico o dentro del producto. El uso continuado después de que los cambios entren en vigor constituye tu
            aceptación de los términos actualizados.
          </p>
        </section>

        <section class="legal-section">
          <h2>13. Contacto</h2>
          <p>
            Para cualquier pregunta sobre estos Términos y Condiciones, contáctanos en:
          </p>
          <address class="legal-address">
            <strong>Espejel Studio</strong><br />
            Operado por Alberto Espejel<br />
            <a href="mailto:alberto@espejelstudio.dev">alberto@espejelstudio.dev</a><br />
            espejelstudio.dev
          </address>
        </section>

      </div>
    </div>
  </main>
</template>

<style scoped>
.legal-page {
  padding: 64px 0 96px;
}

.legal-page__container {
  max-width: 720px;
}

.legal-page__header {
  margin-bottom: 56px;
}

.legal-page__back {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  font-size: 13px;
  font-weight: 500;
  color: var(--color-gray-500);
  margin-bottom: 24px;
  transition: color 0.15s;
}

.legal-page__back:hover {
  color: var(--color-black);
}

.legal-page__title {
  font-size: clamp(28px, 4vw, 40px);
  font-weight: 700;
  letter-spacing: -0.02em;
  color: var(--color-black);
  margin-bottom: 10px;
}

.legal-page__meta {
  font-size: 14px;
  color: var(--color-gray-400);
}

.legal-page__body {
  display: flex;
  flex-direction: column;
  gap: 40px;
}

.legal-section h2 {
  font-size: 17px;
  font-weight: 700;
  color: var(--color-black);
  margin-bottom: 12px;
  letter-spacing: -0.01em;
}

.legal-section p {
  font-size: 15px;
  color: var(--color-gray-500);
  line-height: 1.75;
  margin-bottom: 12px;
}

.legal-section p:last-child {
  margin-bottom: 0;
}

.legal-section ul {
  display: flex;
  flex-direction: column;
  gap: 6px;
  margin: 12px 0;
}

.legal-section ul li {
  font-size: 15px;
  color: var(--color-gray-500);
  line-height: 1.65;
  padding-left: 20px;
  position: relative;
}

.legal-section ul li::before {
  content: '–';
  position: absolute;
  left: 0;
  color: var(--color-gray-300);
}

.legal-address {
  font-style: normal;
  font-size: 15px;
  color: var(--color-gray-500);
  line-height: 1.9;
  margin-top: 12px;
}

.legal-address a {
  color: var(--color-black);
  text-decoration: underline;
  text-underline-offset: 3px;
}
</style>
