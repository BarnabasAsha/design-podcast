<template>
  <div class="container">
    <Header />
    <Hero />
    <Footer />
    <div class="overlay"></div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Hero from "./components/Hero.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Hero,
    Footer,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=DM+Sans:ital,wght@0,400;0,500;0,700;1,400;1,500;1,700&display=swap");

@font-face {
  font-family: Chapaza;
  src: url("./assets/fonts/Chapaza.ttf");
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: "DM Sans", sans-serif;
  background: #ffffff;
  overflow-x: hidden;
}

ul {
  list-style: none;
}

a {
  color: inherit;
  text-decoration: none;
}

h1,
h2,
h3,
h4 {
  font-family: Chapaza, serif;
}

.container {
  width: 100%;
  max-width: 1380px;
  margin: 0 auto;
  padding: 0 2em;
}

.overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  visibility: hidden;
  background: #a13a3f;
  z-index: 2000;
  animation: slideup 1000ms;
  transition: all ease-in 1s;
  animation-iteration-count: 2;
}

@keyframes slideup {
  from {
    height: 100vh;
    visibility: visible;
  }
  to {
    height: 0vh;
    visibility: visible;
  }
}
</style>
