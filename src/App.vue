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

  <header>
    <NavBar />
  </header>
  <main>
    <div class="home-section-container">
      <div class="blobs" aria-hidden="true" role="presentation">
        <div class="blob-right-one"></div>
        <div class="blob-right-two"></div>
      </div>
      <SectionHome id="home" />
    </div>
    <SectionAboutMe id="about" />
    <SectionProjects id="projects" />
    <SectionContacts id="contacts" />
  </main>
  <FooterComponent />
</template>

<style lang="scss">
@import './assets/styles/stars.scss';

.home-section-container {
  position: relative;
  min-height: 100vh;
  overflow-x: clip;
}

header {
  display: flex;
  justify-self: center;
  margin-block-start: 40px;
  position: sticky;
  top: 40px;
  z-index: 5;
}

.blobs {
  position: absolute; /* fix position relative to viewport */
  top: 0;
  left: 0;
  width: 100vw; /* full viewport width */
  height: 100vh; /* full viewport height */
  pointer-events: none; /* allow clicks through */
  z-index: 0; /* behind main content */
}

.blob-right-one {
  position: absolute;
  background-image: url('@/assets/images/right-blob-one.svg');
  width: 350px;
  height: 520px;
  right: calc(-70px);
  bottom: calc(-260px);
  background-repeat: no-repeat;
  background-size: contain;
  opacity: 0.5;
}

.blob-right-two {
  position: absolute;
  background-image: url('@/assets/images/right-blob-two.svg');
  width: 490px;
  height: 590px;
  right: calc(-125px);
  bottom: calc(-250px);
  background-repeat: no-repeat;
  background-size: contain;
  opacity: 0.5;
}
</style>
