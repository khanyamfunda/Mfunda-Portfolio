<script setup>
import ecommerceImage from '../assets/E-com.png'
import firstProductImage from '../assets/first-product.png'
import galleryImage from '../assets/Gallery.png'
import hrImage from '../assets/HR.png'
import portfolioImage from '../assets/portfolio.png'
import productImage from '../assets/product.png'

const projects = [
  { title: 'Product Webpage', image: productImage, description: 'A product page that introduced me to Bootstrap, CSS Grid, and carousels.', tags: ['HTML', 'BOOTSTRAP'], accent: '#2c9c65', tone: 'mint', link: 'https://github.com/khanyamfunda/bootstrap-store2.git' },
  { title: 'Gallery Webpage', image: galleryImage, description: 'A responsive gallery exploring image overlays, transitions, and layout systems.', tags: ['HTML', 'CSS'], accent: '#d26a8d', tone: 'rose', link: 'https://github.com/khanyamfunda/The-Gallery-HTML.git' },
  { title: 'First Product Webpage', image: firstProductImage, description: 'My first product page, with animated backgrounds, product cards, and hover states.', tags: ['HTML', 'CSS'], accent: '#d28a38', tone: 'amber', link: 'https://github.com/khanyamfunda/Avant-Garde-Product-Page.git' },
  { title: 'HR Webpage', image: hrImage, description: 'A group project that pushed me to connect a Vue frontend with Node.js APIs.', tags: ['Vue.js', 'Node.js'], accent: '#3e78b5', tone: 'blue', link: 'https://github.com/khanyamfunda/Hr-Project-final-repo.git' },
  { title: 'E-Commerce Product Webpage', image: ecommerceImage, description: 'A localized e-commerce platform with storefront, payments, performance tools, and delivery concepts.', tags: ['Vue.js', 'Node.js'], accent: '#3e78b5', tone: 'blue', link: 'https://github.com/Antonio1509/Module-3-Core-Project-E-commerce.git' },
  { title: 'Portfolio Website', image: portfolioImage, description: 'This site: my most ambitious project yet, built to make my HTML and CSS more efficient.', tags: ['HTML', 'CSS', 'Figma'], accent: '#2c9c65', tone: 'mint', link: 'https://github.com/khanyamfunda/Portfolio.git' },
]
</script>

<template>
  <section class="projects-section page-section">
    <div class="section-header"><p class="section-label">03 / PROJECTS</p><h2 class="section-title">Things I've <span class="italic-pink">actually built</span></h2><p class="section-description">Small projects, big lessons. Each one taught me something I didn't know before.</p></div>
    <div class="projects-grid">
      <article v-for="project in projects" :key="project.title" class="project-card">
        <div class="project-image" :class="`project-${project.tone}`"><img :src="project.image" :alt="`${project.title} project preview`"><div class="project-overlay"></div><div class="project-accent" :style="{ background: project.accent }"></div></div>
        <div class="project-content"><h3 class="project-title">{{ project.title }}</h3><p class="project-description">{{ project.description }}</p><div class="project-tags"><span v-for="tag in project.tags" :key="tag" class="tag">{{ tag }}</span></div><a class="project-link" :href="project.link" target="_blank" rel="noreferrer">Git link ↗</a></div>
      </article>
    </div>
  </section>
</template>
