<template>
  <div>
    <div class="container">
      <div class="row">
        <div class="col">
          <div class="songs-card">song</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Songs",
};
</script>

<style lang="scss" scoped>
// @import "../assets/scss/style.scss";
//   background-color: $header-bg-color;
.songs-card {
  height: 400px;
  width: 200px;
  background-color: red;
}
</style>