<script setup></script>

<template>
  <section>
    <div class="section-container">
      <span class="decoration-curly-brackets">{ }</span>
      <div>
        <h3>Hello, my name is <span>Margarida</span> and I'm a</h3>
        <h1><span>Front-End</span><br />Developer</h1>
        <div class="buttons-group">
          <a href="#contacts" class="pink-button">Get in touch</a>
          <a href="./assets/logo.svg" download class="green-button"
            >Resume <i class="fa-solid fa-circle-down"></i
          ></a>
        </div>
      </div>
      <span class="decoration-tags">&lt;/&gt;</span>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.section-container {
  display: grid;
  grid-template-columns: 1fr 1.5fr 1fr;
  text-align: center;
}

.decoration-tags,
.decoration-curly-brackets {
  font-weight: 500;
  opacity: 75%;
  font-size: 5rem;
}

.decoration-curly-brackets {
  color: $green;
  align-self: flex-end;
}

.decoration-tags:hover,
.decoration-curly-brackets:hover {
  animation: tilt-shaking 0.5s ease;
}

.decoration-tags {
  color: $pink;
  align-self: flex-start;
}

@keyframes tilt-shaking {
  0% {
    transform: rotate(0deg);
  }
  25% {
    transform: rotate(5deg);
  }
  50% {
    transform: rotate(0deg);
  }
  75% {
    transform: rotate(-5deg);
  }
  100% {
    transform: rotate(0deg);
  }
}

h1 {
  font-size: 6rem;
  font-weight: 800;
  line-height: 125px;
  letter-spacing: 0.2rem;
  filter: drop-shadow(15px 10px 12px rgba($shadow-color, 0.5));
  span {
    font-weight: 800;
    background: linear-gradient(90deg, $purple, $pink);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    color: transparent;
  }
}

h3 {
  font-size: 1.2rem;
  font-weight: 700;
  filter: drop-shadow(15px 10px 12px rgba($shadow-color, 0.25));
  span {
    font-weight: 700;
    font-size: 1.4rem;
    background: linear-gradient(90deg, $green, $dark-green);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    color: transparent;
  }
}

.buttons-group {
  display: flex;
  align-items: center;
  justify-self: center;
  margin-block-start: 30px;
  gap: 25px;

  .pink-button,
  .green-button {
    padding: 10px 40px;
    border-radius: 50px;
    box-shadow: 0 4px 30px rgba($shadow-color, 0.25);
  }

  .pink-button {
    background-size: 200% auto;
    transition: 0.5s;
    // background: linear-gradient(90deg, $pink, $purple);
    background-image: linear-gradient(45deg, $pink 0%, $purple 51%, $pink 100%);
  }

  .green-button {
    background: linear-gradient(90deg, $dark-green, $green);
    color: $shadow-color;
  }

  .pink-button:hover {
    background-position: right center;
  }

  a {
    color: $white-soft;
    text-transform: uppercase;
    text-decoration: none;
    font-weight: 600;
    font-size: 1rem;
  }
}
</style>
