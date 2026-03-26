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
        <h1 class="legal-page__title">Política de Privacidad</h1>
        <p class="legal-page__meta">Espejel Studio · Última actualización: {{ lastUpdated }}</p>
      </div>

      <div class="legal-page__body">

        <section class="legal-section">
          <h2>1. Quiénes somos</h2>
          <p>
            Esta Política de Privacidad aplica a todos los productos de software operados por Espejel Studio,
            un negocio SaaS independiente dirigido por Alberto Espejel ("nosotros" o "nuestro") en espejelstudio.dev.
          </p>
          <p>
            Tomamos tu privacidad en serio. Esta política explica qué datos personales recopilamos, cómo los usamos
            y cuáles son tus derechos sobre esos datos.
          </p>
        </section>

        <section class="legal-section">
          <h2>2. Datos que recopilamos</h2>
          <p>Dependiendo del producto que uses, podemos recopilar las siguientes categorías de datos:</p>

          <h3>Datos de cuenta e identidad</h3>
          <ul>
            <li>Nombre completo y correo electrónico (al registrar una cuenta).</li>
            <li>Nombre y dirección de facturación (recopilados por Stripe durante el pago).</li>
          </ul>

          <h3>Datos de uso y producto</h3>
          <ul>
            <li>Acciones realizadas dentro de la aplicación (funciones usadas, páginas visitadas, configuraciones cambiadas).</li>
            <li>Datos que importas o conectas a un producto (por ejemplo, datos de ventas en TrackrSeller).</li>
            <li>Datos de registro: dirección IP, tipo de navegador, sistema operativo, URL de referencia y marcas de tiempo.</li>
          </ul>

          <h3>Datos de comunicación</h3>
          <ul>
            <li>Correos o mensajes que envíes a nuestra dirección de soporte.</li>
          </ul>

          <h3>Datos de pago</h3>
          <ul>
            <li>
              La información de pago es manejada íntegramente por Stripe. Solo recibimos un resumen no sensible
              (por ejemplo, los últimos 4 dígitos de la tarjeta, dirección de facturación, estado de suscripción).
              Nunca vemos ni almacenamos números de tarjeta completos.
            </li>
          </ul>
        </section>

        <section class="legal-section">
          <h2>3. Cómo usamos tus datos</h2>
          <p>Usamos los datos que recopilamos para:</p>
          <ul>
            <li>Proveer, operar y mejorar nuestros productos.</li>
            <li>Procesar la facturación y gestionar tu suscripción.</li>
            <li>Enviar correos transaccionales (recibos, restablecimiento de contraseña, actualizaciones de producto).</li>
            <li>Responder solicitudes de soporte y resolver disputas.</li>
            <li>Monitorear y prevenir fraudes o abusos.</li>
            <li>Cumplir con obligaciones legales.</li>
          </ul>
          <p>
            No vendemos tus datos personales a terceros. No usamos tus datos para publicidad
            comportamental en plataformas de terceros.
          </p>
        </section>

        <section class="legal-section">
          <h2>4. Base legal para el tratamiento (GDPR)</h2>
          <p>Donde aplique el GDPR u otra ley de protección de datos similar, procesamos tus datos con las siguientes bases legales:</p>
          <ul>
            <li><strong>Ejecución de contrato</strong> — procesamiento necesario para prestar el servicio al que te suscribiste.</li>
            <li><strong>Interés legítimo</strong> — mejorar nuestros productos y prevenir fraudes.</li>
            <li><strong>Obligación legal</strong> — cumplimiento de leyes aplicables.</li>
            <li><strong>Consentimiento</strong> — cuando solicitamos consentimiento opcional específico (por ejemplo, correos de marketing).</li>
          </ul>
        </section>

        <section class="legal-section">
          <h2>5. Servicios de terceros</h2>
          <p>Usamos los siguientes servicios de terceros para operar nuestros productos. Cada uno tiene su propia política de privacidad:</p>
          <ul>
            <li>
              <strong>Stripe, Inc.</strong> — Procesamiento de pagos. Stripe puede recopilar información de facturación
              y datos de transacciones. Consulta <a href="https://stripe.com/privacy" target="_blank" rel="noopener noreferrer">stripe.com/privacy</a>.
            </li>
            <li>
              <strong>Proveedores de infraestructura y hosting</strong> — Nuestros productos se ejecutan en infraestructura
              en la nube (como Vercel o similares). Estos proveedores procesan datos en nuestro nombre bajo acuerdos de
              procesamiento de datos.
            </li>
            <li>
              <strong>Analítica</strong> — Donde se utilice, empleamos herramientas de analítica respetuosas con la
              privacidad, sin cookies y que no construyen perfiles de usuario ni comparten datos con redes publicitarias.
            </li>
          </ul>
        </section>

        <section class="legal-section">
          <h2>6. Cookies</h2>
          <p>
            Nuestros productos utilizan un conjunto mínimo de cookies, limitado a las necesarias para la autenticación
            y gestión de sesiones. No usamos cookies de seguimiento, cookies publicitarias ni cookies de terceros
            con fines de marketing.
          </p>
          <p>
            Puedes controlar o deshabilitar las cookies a través de la configuración de tu navegador, aunque hacerlo
            puede afectar la funcionalidad de nuestros productos.
          </p>
        </section>

        <section class="legal-section">
          <h2>7. Retención de datos</h2>
          <p>
            Conservamos tus datos personales mientras tu cuenta esté activa o sea necesario para prestar nuestros
            servicios. Cuando eliminas tu cuenta, borramos o anonimizamos tus datos personales dentro de los 90 días
            siguientes, excepto cuando la ley exija su conservación (por ejemplo, los registros fiscales pueden
            conservarse hasta 7 años).
          </p>
        </section>

        <section class="legal-section">
          <h2>8. Seguridad de los datos</h2>
          <p>
            Utilizamos prácticas de seguridad estándar de la industria para proteger tus datos, incluyendo
            cifrado en tránsito (TLS) y en reposo, controles de acceso y hash seguro de contraseñas. Sin embargo,
            ningún sistema es completamente inmune a riesgos. Te recomendamos usar una contraseña fuerte y única,
            y contactarnos de inmediato si sospechas cualquier actividad no autorizada.
          </p>
        </section>

        <section class="legal-section">
          <h2>9. Tus derechos</h2>
          <p>Dependiendo de tu ubicación, puedes tener los siguientes derechos sobre tus datos personales:</p>
          <ul>
            <li><strong>Acceso</strong> — solicitar una copia de los datos personales que tenemos sobre ti.</li>
            <li><strong>Rectificación</strong> — solicitar la corrección de datos inexactos.</li>
            <li><strong>Eliminación</strong> — solicitar la eliminación de tus datos ("derecho al olvido").</li>
            <li><strong>Portabilidad</strong> — solicitar tus datos en un formato legible por máquina.</li>
            <li><strong>Oposición</strong> — oponerte a ciertos tipos de procesamiento (por ejemplo, marketing directo).</li>
          </ul>
          <p>
            Para ejercer cualquiera de estos derechos, contáctanos en alberto@espejelstudio.dev. Responderemos
            en un plazo de 30 días.
          </p>
        </section>

        <section class="legal-section">
          <h2>10. Transferencias internacionales</h2>
          <p>
            Nuestros productos se alojan en infraestructura que puede estar ubicada fuera de tu país. Al usar
            nuestros servicios, reconoces que tus datos pueden procesarse en jurisdicciones con distintas leyes de
            protección de datos. Utilizamos proveedores de servicios que ofrecen protecciones adecuadas para dichas
            transferencias.
          </p>
        </section>

        <section class="legal-section">
          <h2>11. Privacidad de menores</h2>
          <p>
            Nuestros productos no están destinados a personas menores de 16 años. No recopilamos conscientemente
            datos personales de menores. Si crees que un menor nos ha proporcionado datos personales, contáctanos
            y los eliminaremos de inmediato.
          </p>
        </section>

        <section class="legal-section">
          <h2>12. Cambios a esta política</h2>
          <p>
            Podemos actualizar esta Política de Privacidad periódicamente. Cuando realicemos cambios sustanciales,
            te notificaremos por correo electrónico o mediante un aviso dentro del producto. La fecha de "última
            actualización" en la parte superior de esta página refleja cuándo se revisó por última vez la política.
          </p>
        </section>

        <section class="legal-section">
          <h2>13. Contáctanos</h2>
          <p>
            Si tienes preguntas, dudas o solicitudes sobre esta Política de Privacidad o tus datos personales,
            contáctanos en:
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

.legal-section h3 {
  font-size: 14px;
  font-weight: 600;
  color: var(--color-gray-700);
  margin-top: 16px;
  margin-bottom: 8px;
  letter-spacing: 0.01em;
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

.legal-section a {
  color: var(--color-black);
  text-decoration: underline;
  text-underline-offset: 3px;
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
}

/* ── Responsive ──────────────────────────────── */
@media (max-width: 768px) {
  .legal-page {
    padding: 48px 0 72px;
  }

  .legal-page__header {
    margin-bottom: 40px;
  }

  .legal-page__body {
    gap: 32px;
  }
}

@media (max-width: 480px) {
  .legal-page {
    padding: 36px 0 56px;
  }

  .legal-page__header {
    margin-bottom: 28px;
  }

  .legal-page__body {
    gap: 24px;
  }

  .legal-section h2 {
    font-size: 15px;
  }

  .legal-section p,
  .legal-section ul li {
    font-size: 14px;
  }
}
</style>
