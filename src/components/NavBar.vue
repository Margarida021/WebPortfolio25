<script setup></script>

<template>
  <nav>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About me</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="https://juniorcodingconfessions.bearblog.dev/" target="_blank">Blog</a></li>
      <li><a href="#contacts">Contacts</a></li>
    </ul>
  </nav>
</template>

<style lang="scss" scoped>
nav {
  display: flex;
  align-items: center;
  width: 1000px;
  height: 60px;
  border: 1px solid $dark-purple-background;
  border-radius: 50px;
  background: rgba(255, 255, 255, 0.15);
  box-shadow: 0 4px 30px rgba($shadow-color, 0.25);
  backdrop-filter: blur(7.1px);
  -webkit-backdrop-filter: blur(7.1px);
}

ul {
  display: inline-flex;
  justify-content: space-around;
  width: 100%;
  padding: 0;
}

a {
  color: $white-soft;
  font-weight: 600;
  font-size: 1.2rem;
  transition: 0.2s ease;
}

a:hover,
a:active,
a:focus-visible {
  color: $dark-green;
}
</style>
