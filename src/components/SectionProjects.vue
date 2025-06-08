<script setup>
import ProjectCard from './ProjectCard.vue'
</script>

<template>
  <section>
    <h2>PROJECTS</h2>
    <ul>
      <li>React.js</li>
      <li>Vue.js</li>
      <li>Ruby on Rails</li>
    </ul>
    <!-- loop para criar diferentes cards -->
    <div class="cards-container">
      <ProjectCard />
    </div>
  </section>
</template>

<style lang="scss" scoped>
.cards-container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 15px;
}
</style>
