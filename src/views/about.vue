<script setup>
import portrait from '../assets/about-portrait.jpg'
</script>

<template>
  <section class="about-section page-section">
    <div class="about-container">
      <div class="about-portrait">
        <img :src="portrait" alt="Khanya Mfunda smiling in a burgundy jacket">
        <small>LEARNING<br>IN PUBLIC</small>
      </div>
      <div class="about-text">
        <p class="section-label">01 / ABOUT ME</p>
        <h2 class="section-title">Who I am &<br><span class="italic-purple">where I'm going</span></h2>
        <div class="about-paragraphs">
          <p>I'm Khanya Mfunda, a 19-year-old web developer in training based in Cape Town, RSA. I discovered coding last year and have been hooked ever since.</p>
          <p>I'm currently being trained by The Life Choices Academy Full-Stack Web Programme, building real webpages and practising code every day.</p>
          <p>Outside of tech, I love fashion, listening to hip-hop, and trying new food spots. I believe creativity and coding go hand-in-hand.</p>
        </div>
        <div class="stats-grid">
          <div class="stat-card"><div class="stat-number">6+</div><div class="stat-label">MONTHS CODING</div></div>
          <div class="stat-card"><div class="stat-number">6</div><div class="stat-label">PROJECTS BUILT</div></div>
          <div class="stat-card"><div class="stat-number">∞</div><div class="stat-label">STILL CURIOUS</div></div>
        </div>
      </div>
    </div>
  </section>
</template>
