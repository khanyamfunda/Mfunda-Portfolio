<script setup>
import { ref } from 'vue'

const submitted = ref(false)
const submittedName = ref('')
const form = ref({ name: '', email: '', message: '' })

function submitForm() {
  submittedName.value = form.value.name
  submitted.value = true
  form.value = { name: '', email: '', message: '' }
}
</script>

<template>
  <section class="contact-section page-section">
    <div class="section-header"><p class="section-label">04 / CONTACT</p><h2 class="section-title">Let's <span class="italic-pink">say hi</span></h2><p class="section-description">Whether you want to offer mentorship, give feedback, or just talk tech, my inbox is always open.</p></div>
    <div class="contact-container">
      <form class="contact-form" @submit.prevent="submitForm">
        <div class="form-group"><label for="name">YOUR NAME</label><input id="name" v-model="form.name" type="text" placeholder="e.g. Jordan Lee" required></div>
        <div class="form-group"><label for="email">EMAIL</label><input id="email" v-model="form.email" type="email" placeholder="you@example.com" required></div>
        <div class="form-group"><label for="message">MESSAGE</label><textarea id="message" v-model="form.message" rows="5" placeholder="Say something nice..." required></textarea></div>
        <button type="submit" class="btn-submit">Send message <span>↗</span></button>
        <p v-if="submitted" class="form-success">Thanks, {{ submittedName || 'friend' }}. Your message is ready to send.</p>
      </form>
      <div class="contact-info"><div class="contact-box"><p class="contact-box-label">CURRENTLY AVAILABLE FOR</p><p class="contact-box-text">Internships & mentorship</p><div class="status-indicator"><div class="status-dot"></div><span>Open to opportunities</span></div></div><div class="social-links"><p class="social-label">FIND ME ONLINE</p><a class="social-link" href="https://github.com/khanyamfunda" target="_blank" rel="noreferrer">GitHub <span>↗</span></a><a class="social-link" href="https://www.linkedin.com/in/khanya-mfunda-1887bb413" target="_blank" rel="noreferrer">LinkedIn <span>↗</span></a><a class="social-link" href="mailto:khanyamfunda9@gmail.com">Email <span>↗</span></a></div></div>
    </div>
  </section>
</template>
