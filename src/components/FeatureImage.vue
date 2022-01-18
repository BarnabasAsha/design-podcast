<template>
  <div class="feature">
    <div class="feature_image" :style="cssVar">
      <img :src="require(`../assets/images/${imgsrc}`)" :alt="artist" />
    </div>
    <div class="feature_artist">{{ artist }}</div>
  </div>
</template>

<script>
export default {
  name: "FeatureImage",
  props: {
    imgsrc: String,
    artist: String,
    color: String,
  },
  computed: {
    cssVar: function () {
      return {
        "--bg-color": this.color,
      };
    },
  },
};
</script>

<style scoped>
.feature {
  margin-right: 30px;
}
.feature_image {
  position: relative;
  width: 180px;
  height: 180px;
  border-radius: 6px;
  opacity: 0;
  transform-origin: bottom;
  animation: slideup 1000ms;
  transition: all ease-in 1s;
  animation-delay: 4000ms;
  animation-fill-mode: forwards;
}

.feature_image:after {
  content: "";
  width: 100%;
  height: 100%;
  position: absolute;
  border-radius: 6px;
  background: var(--bg-color);
  bottom: -5px;
  right: -5px;
  bottom: 0;
  transform-origin: bottom;
  filter: drop-shadow(5px 5px 50px rgba(0, 0, 0, 0.3));
  z-index: 1;
  opacity: 0;
  animation: slideup 500ms;
  transition: all ease-in 1s;
  animation-delay: 5000ms;
  animation-fill-mode: forwards;
}

.feature_image img {
  position: relative;
  z-index: 2;
  width: 100%;
  height: 100%;
  border-radius: 6px;
}

.feature_artist {
  font-size: 18px;
  line-height: 23px;
  letter-spacing: -0.4px;
  margin-top: 0.9em;
  opacity: 0;
  animation: show 1000ms;
  transition: all ease-in 1s;
  animation-delay: 4500ms;
  animation-fill-mode: forwards;
}

@keyframes slideup {
  from {
    opacity: 0;
    transform: scaleY(0%);
  }
  to {
    opacity: 1;
    transform: scaleY(100%);
  }
}

@keyframes show {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@media (max-width: 700px) {
  .feature {
    margin-right: 0px;
    margin: 15px 0;
  }
}
</style>
