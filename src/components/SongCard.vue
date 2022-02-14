<template>
  <div class="song-card text-center p-3">
    <figure>
      <img :src="matteo.poster" :alt="matteo.title" class="img-fluid" />
    </figure>
    <div class="song-desc">
      <h4>{{ matteo.title }}</h4>
      <p>{{ matteo.author }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "SongCard",
  props: ["matteo"],
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/-var.scss";
.song-card {
  height: 340px;
  background-color: $header-bg-color;
  .song-desc {
    h4 {
      color: white;
      text-transform: uppercase;
    }
    p {
      color: darkgray;
    }
  }
}
</style>