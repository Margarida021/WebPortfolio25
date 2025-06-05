<script setup>
import NavBar from './components/NavBar.vue'
import SectionHome from './components/SectionHome.vue'
import SectionAboutMe from './components/SectionAboutMe.vue'
import SectionProjects from './components/SectionProjects.vue'
import SectionContacts from './components/SectionContacts.vue'
import FooterComponent from './components/FooterComponent.vue'
</script>

<template>
  <!-- <div class="sparkles">
    <span
      v-for="n in 30"
      :key="n"
      class="sparkle"
      :style="{
        top: `${Math.random() * 100}vh`,
        left: `${Math.random() * 100}vw`,
        animationDelay: `${Math.random() * 5}s`,
        animationDuration: `${2 + Math.random() * 3}s`,
      }"
    />
  </div> -->
  <div class="sparkles">
    <span
      v-for="(n, i) in 50"
      :key="i"
      class="sparkle"
      :style="{
        top: `${Math.floor(i / 10) * 20 + Math.random() * 5}vh`,
        left: `${(i % 10) * 10 + Math.random() * 5}vw`,
        animationDelay: `${Math.random() * 6}s`,
        animationDuration: `${5 + Math.random() * 5}s`,
        transform: `scale(${0.7 + Math.random() * 0.9})`,
      }"
    />
  </div>
  <!-- <div class="sparkles">
    <span class="sparkle s1"></span>
    <span class="sparkle s2"></span>
    <span class="sparkle s3"></span>
  </div> -->
  <div class="blobs">
    <div class="blob-right-one"></div>
    <div class="blob-right-two"></div>
  </div>
  <header>
    <NavBar />
  </header>
  <main>
    <SectionHome id="home" />
    <SectionAboutMe id="about" />
    <SectionProjects id="projects" />
    <SectionContacts id="contacts" />
  </main>
  <FooterComponent />
</template>

<style lang="scss">
@import './assets/stars.scss';

header {
  display: flex;
  justify-self: center;
  margin-block-start: 40px;
}
</style>
