<template>
  <header>
    <div class="header">
      <Logo />
      <nav>
        <ul>
          <li>
            <a href="#">About</a>
          </li>
          <li>
            <a href="#">Interviews</a>
          </li>
          <li>
            <a href="#" class="active">Episodes</a>
          </li>
          <li>
            <a href="#">Mixtapes</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
import Logo from "../components/Logo.vue";

export default {
  name: "Header",
  components: {
    Logo,
  },
};
</script>

<style scoped>
.header {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 2em 0;
  animation: slidedown 1000ms;
  animation-delay: 1000ms;
  animation-fill-mode: forwards;
  transition: all ease-in 1s;
  opacity: 0;
}

.header nav ul {
  display: flex;
  justify-content: flex-start;
  align-items: center;
}

.header nav li {
  margin-left: 50px;
}

.header nav a {
  font-size: 1.1rem;
  line-height: 1.5rem;
  letter-spacing: -0.4px;
  color: #333333;
}

.header nav a.active {
  color: #a13a3f;
  font-weight: bold;
  position: relative;
}

.header nav a.active::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 7px;
  background: #a13a3f;
  opacity: 0.2;
  background-blend-mode: normal;
}

@keyframes slidedown {
  from {
    transform: translateY(-60%);
    opacity: 0;
  }
  to {
    transform: translateY(0);
    opacity: 1;
  }
}

@media (max-width: 700px) {
  .header nav {
    display: none;
  }
}
</style>
