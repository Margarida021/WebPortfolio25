<script setup></script>

<template>
  <footer>
    <div class="line-text-group">
      <div class="line" role="presentation" aria-hidden="true"></div>
      <p>2025 WebPortfolio</p>
    </div>
    <div class="mouse-scroll-icon"></div>
    <ul>
      <li>Icon</li>
      <li>Icon</li>
      <li>Icon</li>
    </ul>
  </footer>
</template>

<style lang="scss" scoped>
footer {
  position: sticky;
  bottom: 0;
  z-index: 1;
  text-align: center;
  width: 100%;
  display: inline-flex;
  align-items: center;
  justify-content: center;
}

.line-text-group {
  display: inline-flex;
  align-items: center;
  gap: 5px;
}

.line {
  width: 50px;
  height: 0;
  border: 2px solid $green;
}

.mouse-scroll-icon {
  width: 25px;
  height: 40px;
  border: 2px solid $white-soft;
  position: relative;
  border-radius: 50px;
}

.mouse-scroll-icon::before {
  content: '';
  position: absolute;
  top: 8px;
  width: 4px;
  height: 4px;
  background-color: $white-soft;
  border-radius: 50%;
  animation: scroll-dot 2s ease-in-out infinite;
}

@keyframes scroll-dot {
  0% {
    opacity: 1;
    transform: translate(-50%, 0);
  }
  100% {
    opacity: 0;
    transform: translate(-50%, 15px);
  }
}
</style>
