<template>
  <div class="hero_grid">
    <div class="hero_grid_g1">
      <img src="../assets/images/gustavo.png" alt="" />
    </div>
    <div class="hero_grid_g2">
      <img src="../assets/images/martino.png" alt="" />
    </div>
    <div class="hero_grid_g3">
      <img src="../assets/images/vlad.png" alt="" />
    </div>
    <div class="hero_grid_g4">
      <img src="../assets/images/kirill.png" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  name: "hero_grid",
};
</script>

<style scoped>
.hero_grid {
  margin-left: 1em;
  width: 100%;
  height: 700px;
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-template-rows: repeat(7, 1fr);
  grid-template-areas:
    "...... grid_one grid_one grid_one ......"
    "...... grid_one grid_one grid_one ......"
    "grid_two grid_two grid_three grid_three grid_three"
    "grid_two grid_two grid_three grid_three grid_three"
    "grid_two grid_two grid_four grid_four ......"
    "....... ....... grid_four grid_four ......"
    "....... ....... grid_four grid_four ......";
  opacity: 0;
  animation: slideup 1000ms;
  transition: all ease-in 1s;
  animation-delay: 6000ms;
  animation-fill-mode: forwards;
}

.hero_grid img {
  width: 100%;
  height: auto;
}

.hero_grid_g1 {
  grid-area: grid_one;
  filter: drop-shadow(50px 50px 200px rgba(161, 58, 63, 0.25));
}

.hero_grid_g2 {
  grid-area: grid_two;
  position: relative;
  z-index: 3;
  filter: drop-shadow(50px 50px 200px #abadad);
  transform: translateY(-20px);
}

.hero_grid_g3 {
  grid-area: grid_three;
  position: relative;
  z-index: 4;
  filter: drop-shadow(50px 50px 200px #bbcdd4);
}

.hero_grid_g4 {
  grid-area: grid_four;
  position: relative;
  z-index: 1;
  transform: translateY(-80px);
  filter: drop-shadow(50px 50px 200px #bac7cd);
}

@keyframes slideup {
  from {
    opacity: 0;
    transform: translateY(100%);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
