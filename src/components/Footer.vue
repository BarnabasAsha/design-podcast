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
}

.footer ul {
  display: flex;
  align-items: center;
}

.footer li {
  margin-right: 2.5em;
}
</style>
