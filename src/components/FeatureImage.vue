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
}

.feature_image:after {
  content: "";
  width: 100%;
  height: 100%;
  position: absolute;
  border-radius: 6px;
  background: var(--bg-color);
  top: 0;
  left: 0;
  bottom: 0;
  transform: translate(5px, 5px);
  filter: drop-shadow(5px 5px 50px rgba(0, 0, 0, 0.3));
  z-index: 1;
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
}

@media (max-width: 700px) {
  .feature {
    margin-right: 0px;
    margin: 15px 0;
  }
}
</style>
