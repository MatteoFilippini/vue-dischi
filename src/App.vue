<template>
  <div>
    <header>
      <figure>
        <img src="./assets/img/logo-spotify.jpg" alt="logo" />
      </figure>
    </header>
    <main class="text-center">main</main>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
};
</script>

<style lang="scss">
// importo bootstrap
@import "bootstrap";
// importo tutto il css
@import "./assets/scss/style.scss";

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
header {
  height: 50px;
  background-color: $header-bg-color;
}
main {
  height: calc(100vh - 50px);
  background-color: $main-bg-color;
  color: white;
}
img {
  height: 50px;
}
</style>
