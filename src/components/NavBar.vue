<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'
import { RouterLink } from 'vue-router'

const scrolled = ref(false)
const menuOpen = ref(false)

function onScroll() {
  scrolled.value = window.scrollY > 16
}

function toggleMenu() {
  menuOpen.value = !menuOpen.value
}

function closeMenu() {
  menuOpen.value = false
}

onMounted(() => window.addEventListener('scroll', onScroll))
onBeforeUnmount(() => window.removeEventListener('scroll', onScroll))
</script>

<template>
  <header class="navbar" :class="{ 'navbar--scrolled': scrolled }">
    <div class="container navbar__inner">
      <RouterLink to="/" class="navbar__logo" @click="closeMenu">
        <span class="navbar__logo-mark">ES</span>
        <span class="navbar__logo-text">Espejel Studio</span>
      </RouterLink>

      <nav class="navbar__nav" :class="{ 'navbar__nav--open': menuOpen }">
        <a href="/#products" class="navbar__link" @click="closeMenu">Productos</a>
        <a href="/#about" class="navbar__link" @click="closeMenu">Nosotros</a>
        <a href="/#contact" class="navbar__link" @click="closeMenu">Contacto</a>
        <a href="/#contact" class="btn btn--primary navbar__cta" @click="closeMenu">Escríbenos</a>
      </nav>

      <button class="navbar__hamburger" :class="{ 'is-open': menuOpen }" @click="toggleMenu" aria-label="Toggle menu">
        <span></span>
        <span></span>
        <span></span>
      </button>
    </div>
  </header>
</template>

<style scoped>
.navbar {
  position: sticky;
  top: 0;
  z-index: 100;
  background-color: rgba(255, 255, 255, 0.92);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease, box-shadow 0.2s ease;
}

.navbar--scrolled {
  border-bottom-color: var(--color-gray-200);
  box-shadow: 0 1px 0 rgba(0,0,0,0.04);
}

.navbar__inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 60px;
}

.navbar__logo {
  display: flex;
  align-items: center;
  gap: 10px;
  font-weight: 600;
  font-size: 15px;
  color: var(--color-black);
  letter-spacing: -0.01em;
}

.navbar__logo-mark {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 30px;
  height: 30px;
  background-color: var(--color-black);
  color: var(--color-white);
  font-size: 11px;
  font-weight: 700;
  letter-spacing: 0.04em;
  border-radius: var(--radius-sm);
  flex-shrink: 0;
}

.navbar__nav {
  display: flex;
  align-items: center;
  gap: 4px;
}

.navbar__link {
  font-size: 14px;
  font-weight: 500;
  color: var(--color-gray-500);
  padding: 6px 12px;
  border-radius: var(--radius-sm);
  transition: color 0.15s ease, background-color 0.15s ease;
}

.navbar__link:hover {
  color: var(--color-black);
  background-color: var(--color-gray-100);
}

.navbar__cta {
  margin-left: 8px;
  font-size: 14px;
  padding: 8px 16px;
}

.navbar__hamburger {
  display: none;
  flex-direction: column;
  gap: 5px;
  padding: 6px;
  cursor: pointer;
  background: none;
  border: none;
}

.navbar__hamburger span {
  display: block;
  width: 22px;
  height: 1.5px;
  background-color: var(--color-black);
  transition: transform 0.2s ease, opacity 0.2s ease;
  border-radius: 2px;
}

.navbar__hamburger.is-open span:nth-child(1) {
  transform: translateY(6.5px) rotate(45deg);
}
.navbar__hamburger.is-open span:nth-child(2) {
  opacity: 0;
}
.navbar__hamburger.is-open span:nth-child(3) {
  transform: translateY(-6.5px) rotate(-45deg);
}

@media (max-width: 720px) {
  .navbar__hamburger {
    display: flex;
  }

  .navbar__nav {
    display: none;
    position: absolute;
    top: 60px;
    left: 0;
    right: 0;
    flex-direction: column;
    align-items: stretch;
    background-color: var(--color-white);
    border-bottom: 1px solid var(--color-gray-200);
    padding: 12px 24px 20px;
    gap: 4px;
  }

  .navbar__nav--open {
    display: flex;
  }

  .navbar__link {
    padding: 10px 12px;
  }

  .navbar__cta {
    margin-left: 0;
    margin-top: 8px;
    text-align: center;
  }
}
</style>
