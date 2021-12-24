<template>
  <div class="hero">
    <div class="hero_left">
      <h5>Episode 13</h5>
      <h1>Art & Design</h1>
      <p>
        The dichotomy of art & design is often talked about but rarely
        understood, in this episode we dive in to what art and design really
        are, what kind of weight do they hold and their overall impact on the
        human condition.
      </p>
      <div class="hero_left_feature">
        <h4>Featuring</h4>
        <div class="hero_left_feature-flex">
          <FeatureImage
            v-for="feature in features"
            v-bind:key="feature.color"
            v-bind:imgsrc="feature.src"
            v-bind:artist="feature.artist"
            v-bind:color="feature.color"
          />
        </div>
      </div>
    </div>
    <div class="hero_right">
      <HeroGrid />
      <button class="hero_right_play" title="play">
        <img src="../assets/images/PLAY.svg" alt="play" />
      </button>
    </div>
  </div>
</template>

<script>
import FeatureImage from "../components/FeatureImage.vue";
import HeroGrid from "../components/HeroGrid.vue";
import featureJson from "../data/features.json";

export default {
  name: "Hero",
  components: {
    FeatureImage,
    HeroGrid,
  },
  data() {
    return {
      features: featureJson,
    };
  },
};
</script>

<style scoped>
.hero {
  margin-top: 2em;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
}

.hero_left {
  width: 50%;
}

.hero_right {
  width: 45%;
  position: relative;
}

.hero_right_play {
  width: 480px;
  height: 480px;
  position: absolute;
  background: none;
  border: none;
  outline: none;
  left: 50%;
  margin-left: -150px;
  top: 50%;
  margin-top: -270px;
  z-index: 20;
  cursor: pointer;
  filter: drop-shadow(25px 25px 200px rgba(0, 0, 0, 0.5));
}

.hero_left h5 {
  font-weight: bold;
  font-size: 1rem;
  line-height: 1.5rem;
  letter-spacing: -0.94px;
  color: #333333;
  margin-bottom: 1em;
}

.hero_left h1 {
  font-size: 3rem;
  color: #000000;
}

.hero_left p {
  font-size: 1.2rem;
  line-height: 36px;
  letter-spacing: 0.2px;
  color: #333333;
  margin: 1em 0 1em 0;
}

.hero_left_feature {
  margin-top: 2.5em;
}

.hero_left_feature h4 {
  margin-bottom: 1em;
  font-size: 1.25rem;
  letter-spacing: 0.52px;
}

.hero_left_feature-flex {
  display: flex;
}

@media (max-width: 700px) {
  .hero_left {
    width: 100%;
  }

  .hero_right {
    display: none;
  }

  .hero_left h1 {
    font-size: 2.8rem;
  }

  .hero_left_feature-flex {
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
}
</style>
