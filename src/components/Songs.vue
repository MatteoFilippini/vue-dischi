<template>
  <div>
    <div class="container">
      <div class="row">
        <div class="col-2 p-2" v-for="(song, index) in songs" :key="index">
          <div class="song-card text-center p-3">
            <figure>
              <img :src="song.poster" :alt="song.title" class="img-fluid" />
            </figure>
            <div class="song-desc">
              <h4>{{ song.title }}</h4>
              <p>{{ song.author }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Songs",
  props: ["songs"],
};
</script>

<style lang="scss" scoped>
// @import "../assets/scss/style.scss";
//   background-color: $header-bg-color;
.song-card {
  height: 340px;
  background-color: red;
  .song-desc {
    h4 {
      color: white;
      text-transform: uppercase;
    }
    p {
      color: blue;
    }
  }
}
</style>