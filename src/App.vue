<template>
  <div>
    <header>
      <figure>
        <img src="./assets/img/logo-spotify.jpg" alt="logo" />
      </figure>
    </header>
    <main class="text-center">
      <Songs :songs="songs" />
    </main>
  </div>
</template>

<script>
import axios from "axios";

import Songs from "./components/Songs.vue";
export default {
  name: "App",
  components: {
    Songs,
  },
  data() {
    return {
      songs: [],
    };
  },
  methods: {
    getSongs() {
      axios
        .get("https://flynn.boolean.careers/exercises/api/array/music")
        .then((res) => {
          this.songs = res.data.response;
        });
    },
  },
  mounted() {
    this.getSongs();
  },
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
  height: 100%;
  background-color: $main-bg-color;
  color: white;
  padding: 50px 0;
}
img {
  height: 50px;
}
</style>
