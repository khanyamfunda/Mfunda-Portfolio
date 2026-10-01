<script setup>
import { computed } from 'vue'

const skills = [
  { name: 'HTML', note: 'Built a product page from scratch', percent: 75, group: 'Languages', color: '#2c9c65' },
  { name: 'CSS', note: 'Learning Flexbox, Grid, and animations', percent: 65, group: 'Languages', color: '#2c9c65' },
  { name: 'JavaScript', note: 'Functions, arrays, conditionals, and error handling', percent: 50, group: 'Languages', color: '#2c9c65' },
  { name: 'MySQL', note: 'Database design, modeling, and data manipulation', percent: 90, group: 'Languages', color: '#2c9c65' },
  { name: 'PHP', note: 'Database connections and dynamic web creation', percent: 60, group: 'Languages', color: '#2c9c65' },
  { name: 'Node.js', note: 'Requests, responses, APIs, and routing frameworks', percent: 80, group: 'Languages', color: '#2c9c65' },
  { name: 'Python', note: 'Programming logic and simple scripts', percent: 60, group: 'Languages', color: '#2c9c65' },
  { name: 'VS Code', note: 'My daily driver, getting comfortable with extensions', percent: 90, group: 'Tools & Platforms', color: '#d26a38' },
  { name: 'Git & GitHub', note: 'Commits, branches, and pull requests', percent: 85, group: 'Tools & Platforms', color: '#d26a38' },
  { name: 'Terminal / CLI', note: 'Basic commands and navigating directories', percent: 55, group: 'Tools & Platforms', color: '#d26a38' },
]

const groups = computed(() => [...new Set(skills.map((skill) => skill.group))])
</script>

<template>
  <section class="skills-section page-section">
    <div class="section-header"><p class="section-label">02 / SKILLS</p><h2 class="section-title">What I've <span class="italic-purple">picked up so far</span></h2><p class="section-description">Still early in my journey. These bars are honest, and I'm proud of every percentage point.</p></div>
    <div class="skills-content">
      <div v-for="group in groups" :key="group">
        <h3 class="skills-category">{{ group }}</h3>
        <div class="skills-list">
          <div v-for="skill in skills.filter((item) => item.group === group)" :key="skill.name" class="skill-item">
            <div class="skill-header"><div><span class="skill-name">{{ skill.name }}</span><span class="skill-note">— {{ skill.note }}</span></div><span class="skill-percent" :style="{ color: skill.color }">{{ skill.percent }}%</span></div>
            <div class="skill-bar"><div class="skill-fill" :style="{ width: `${skill.percent}%`, background: skill.color }"></div></div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
