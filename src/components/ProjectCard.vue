<script setup>
import projects from '@/projectsData.json'

console.log(projects)
</script>

<template>
  <div class="project-card" v-for="project in projects" :key="project.id">
    <!-- <img src="{{project.image}}" /> -->
    <p class="title">{{ project.title }}</p>
    <p class="description">{{ project.description }}</p>
    <ul>
      <li>HTML</li>
      <li>CSS</li>
      <li>JavaScript</li>
      <li>React</li>
    </ul>
    <button>See more!</button>
  </div>
</template>

<style lang="scss" scoped>
.project-card {
  background-color: $dark-blue-card-background;
  border: 1px solid $pink;
  border-radius: 35px;
  text-align: center;
}

.title {
  text-transform: uppercase;
}
</style>
