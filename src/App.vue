<template>
  <div>
    <header>
      <!-- <figure><img src="../assets/img/logo.png" alt="logo" /></figure> -->
    </header>
    <main>main</main>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {},
};
</script>

<style lang="scss">
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
  height: 100vh;
  background-color: $main-bg-color;
}
</style>
