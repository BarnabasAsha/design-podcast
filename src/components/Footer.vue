<template>
  <footer>
    <div class="footer">
      <h4>Share</h4>
      <ul>
        <li>
          <a title="url" href="#">
            <img src="../assets/images/LINK.svg" alt="url" />
          </a>
        </li>
        <li>
          <a title="facebook" href="#">
            <img src="../assets/images/FB.svg" alt="facebook" />
          </a>
        </li>
        <li>
          <a title="twitter" href="#">
            <img src="../assets/images/TW.svg" alt="twitter" />
          </a>
        </li>
      </ul>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style scoped>
.footer {
  width: 100%;
  margin: 2em 0;
}
.footer h4 {
  margin-bottom: 1em;
  font-size: 1.25rem;
  letter-spacing: 0.52px;
  opacity: 0;
  animation: slidedown 500ms;
  transition: all ease-in 1s;
  animation-delay: 4000ms;
  animation-fill-mode: forwards;
}

.footer ul {
  display: flex;
  align-items: center;
}

.footer li {
  margin-right: 2.5em;
}

.footer li a:nth-child(1) {
  opacity: 0;
  animation: show 1000ms;
  transition: all ease-in 1s;
  animation-delay: 5500ms;
  animation-fill-mode: forwards;
}

.footer li a:nth-child(2) {
  opacity: 0;
  animation: show 1000ms;
  transition: all ease-in 1s;
  animation-delay: 6500ms;
  animation-fill-mode: forwards;
}

.footer li a:nth-child(3) {
  opacity: 0;
  animation: show 1000ms;
  transition: all ease-in 1s;
  animation-delay: 7500ms;
  animation-fill-mode: forwards;
}

@keyframes slidedown {
  from {
    transform: translateY(-30px);
    opacity: 0;
  }
  to {
    transform: translateY(0);
    opacity: 1;
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
</style>
