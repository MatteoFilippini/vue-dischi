<template>
  <div>
    <header>header</header>
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

header {
  height: 50px;
  background-color: $header-bg-color;
}
</style>
