<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)

const pages = [
  { name: 'Home', path: '/' },
  { name: 'About', path: '/about' },
  { name: 'Skills', path: '/skills' },
  { name: 'Projects', path: '/projects' },
  { name: 'Contact', path: '/contact' },
]

function closeMenu() {
  menuOpen.value = false
}
</script>

<template>
  <header class="navbar" :class="{ 'menu-is-open': menuOpen }">
    <nav class="nav-container">
      <RouterLink class="logo" to="/" aria-label="Go to home" @click="closeMenu">
        <span class="logo-icon">&lt;/&gt;</span>
        <span class="logo-text">Khanya<span class="logo-dot">.</span></span>
      </RouterLink>
      <button class="menu-toggle" type="button" :aria-expanded="menuOpen" aria-label="Toggle navigation" @click="menuOpen = !menuOpen">☰</button>
      <div class="nav-links" :class="{ 'is-open': menuOpen }">
        <RouterLink v-for="page in pages" :key="page.path" :to="page.path" active-class="active" @click="closeMenu">{{ page.name }}</RouterLink>
      </div>
    </nav>
  </header>
</template>
