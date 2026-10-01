<script setup>
import { useRouter } from 'vue-router'

const router = useRouter()
</script>

<template>
  <section class="hero-section page-section">
    <div class="bg-grid"></div>
    <div class="glow-blob glow-blob-1"></div>
    <div class="glow-blob glow-blob-2"></div>
    <div class="hero-content">
      <p class="hero-kicker">STUDENT DEVELOPER / CAPE TOWN</p>
      <h1 class="hero-title">Hi, I'm <span class="gradient-text">Khanya Mfunda</span></h1>
      <p class="hero-subtitle">A student exploring the world of tech, building small things, learning big ideas, and figuring it out one line of code at a time.</p>
      <div class="hero-ctas">
        <button class="btn-gradient" type="button" @click="router.push('/projects')">See my work <span>↗</span></button>
        <button class="btn-outline" type="button" @click="router.push('/about')">About me</button>
      </div>
    </div>
    <div class="hero-note">SCROLL TO EXPLORE <span>↓</span></div>
  </section>
</template>
