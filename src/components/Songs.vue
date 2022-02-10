<template>
  <div>
    <div class="container">
      <div class="row">
        <div class="col-2">
          <div class="song-card text-center">
            <figure>
              <img src="../assets/img/logo-spotify.jpg" alt="song" />
            </figure>
            <div class="song-desc">
              <h4>titolo</h4>
              <p>Autore</p>
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
};
</script>

<style lang="scss" scoped>
// @import "../assets/scss/style.scss";
//   background-color: $header-bg-color;
.song-card {
  height: 400px;
  width: 200px;
  background-color: red;
  img {
    height: 180px;
    margin-top: 10px;
  }
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