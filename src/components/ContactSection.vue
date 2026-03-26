<script setup>
import { ref } from 'vue'

const form = ref({
  name: '',
  email: '',
  message: '',
})

const submitted = ref(false)
const error = ref('')

function handleSubmit() {
  if (!form.value.name || !form.value.email || !form.value.message) {
    error.value = 'Por favor completa todos los campos.'
    return
  }
  if (!/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(form.value.email)) {
    error.value = 'Por favor ingresa un correo electrónico válido.'
    return
  }
  error.value = ''
  submitted.value = true
}
</script>

<template>
  <section id="contact" class="section contact">
    <div class="container contact__inner">
      <div class="contact__info">
        <span class="section__label">Contacto</span>
        <h2 class="section__heading">Hablemos.</h2>
        <p class="contact__body">
          ¿Tienes una pregunta sobre algún producto, facturación o una posible colaboración?
          Manda un mensaje y te responderemos a la brevedad.
        </p>

        <div class="contact__details">
          <a href="mailto:alberto@espejelstudio.dev" class="contact__email">
            <svg width="16" height="16" viewBox="0 0 16 16" fill="none" aria-hidden="true">
              <rect x="1.5" y="3.5" width="13" height="9" rx="1.5" stroke="currentColor" stroke-width="1.3"/>
              <path d="M1.5 5.5L8 9.5l6.5-4" stroke="currentColor" stroke-width="1.3" stroke-linecap="round"/>
            </svg>
            alberto@espejelstudio.dev
          </a>
          <p class="contact__note">Operado por Alberto Espejel · espejelstudio.dev</p>
        </div>
      </div>

      <div class="contact__form-wrap">
        <Transition name="fade-form" mode="out-in">
          <div v-if="submitted" class="contact__success" key="success">
            <div class="contact__success-icon" aria-hidden="true">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none">
                <circle cx="12" cy="12" r="10" stroke="#6db88a" stroke-width="1.5"/>
                <path d="M7.5 12l3 3 6-6" stroke="#6db88a" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
            </div>
            <h3 class="contact__success-heading">Mensaje recibido</h3>
            <p class="contact__success-body">Gracias por escribirnos. Responderemos a tu correo en un día hábil.</p>
          </div>

          <form
            v-else
            key="form"
            class="contact__form"
            @submit.prevent="handleSubmit"
            novalidate
          >
            <div class="contact__field">
              <label for="contact-name" class="contact__label">Nombre</label>
              <input
                id="contact-name"
                v-model="form.name"
                type="text"
                class="contact__input"
                placeholder="Tu nombre"
                autocomplete="name"
              />
            </div>

            <div class="contact__field">
              <label for="contact-email" class="contact__label">Correo electrónico</label>
              <input
                id="contact-email"
                v-model="form.email"
                type="email"
                class="contact__input"
                placeholder="tu@correo.com"
                autocomplete="email"
              />
            </div>

            <div class="contact__field">
              <label for="contact-message" class="contact__label">Mensaje</label>
              <textarea
                id="contact-message"
                v-model="form.message"
                class="contact__input contact__textarea"
                placeholder="¿En qué podemos ayudarte?"
                rows="4"
              ></textarea>
            </div>

            <p v-if="error" class="contact__error" role="alert">{{ error }}</p>

            <button type="submit" class="btn btn--primary contact__submit">
              Enviar mensaje
            </button>
          </form>
        </Transition>
      </div>
    </div>
  </section>
</template>

<style scoped>
.contact {
  border-top: 1px solid var(--color-gray-200);
  border-bottom: 1px solid var(--color-gray-200);
}

.contact__inner {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 80px;
  align-items: start;
}

.contact__body {
  font-size: 16px;
  color: var(--color-gray-500);
  line-height: 1.7;
  margin-bottom: 32px;
}

.contact__details {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.contact__email {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  font-size: 15px;
  font-weight: 600;
  color: var(--color-black);
  transition: opacity 0.15s;
}

.contact__email:hover {
  opacity: 0.65;
}

.contact__note {
  font-size: 13px;
  color: var(--color-gray-400);
}

/* Form */
.contact__form {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.contact__field {
  display: flex;
  flex-direction: column;
  gap: 7px;
}

.contact__label {
  font-size: 13px;
  font-weight: 600;
  color: var(--color-gray-700);
  letter-spacing: 0.01em;
}

.contact__input {
  font-family: var(--font-sans);
  font-size: 16px; /* 16px mínimo evita el zoom automático en iOS */
  color: var(--color-black);
  background-color: var(--color-white);
  border: 1.5px solid var(--color-gray-200);
  border-radius: var(--radius-md);
  padding: 11px 14px;
  outline: none;
  transition: border-color 0.18s ease, box-shadow 0.18s ease;
  width: 100%;
  line-height: 1.5;
}

.contact__input::placeholder {
  color: var(--color-gray-300);
}

.contact__input:focus {
  border-color: var(--color-black);
  box-shadow: 0 0 0 3px rgba(0, 0, 0, 0.06);
}

.contact__textarea {
  resize: vertical;
  min-height: 110px;
}

.contact__error {
  font-size: 13px;
  color: #c0392b;
  font-weight: 500;
}

.contact__submit {
  align-self: flex-start;
  padding: 12px 24px;
  font-size: 15px;
}

/* Success state */
.contact__success {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 12px;
  padding: 32px;
  background-color: var(--color-accent-subtle, #eaf7ef);
  border: 1px solid var(--color-accent);
  border-radius: var(--radius-lg);
}

.contact__success-icon {
  margin-bottom: 4px;
}

.contact__success-heading {
  font-size: 17px;
  font-weight: 700;
  color: var(--color-black);
}

.contact__success-body {
  font-size: 14px;
  color: var(--color-gray-500);
  line-height: 1.6;
}

.fade-form-enter-active,
.fade-form-leave-active {
  transition: opacity 0.25s ease;
}
.fade-form-enter-from,
.fade-form-leave-to {
  opacity: 0;
}

@media (max-width: 860px) {
  .contact__inner {
    grid-template-columns: 1fr;
    gap: 48px;
  }
}
</style>
