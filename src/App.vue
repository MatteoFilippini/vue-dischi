<template>
  <div>
    <header>
      <Logo />
      <Select :pincopallino="songs" @genere="findSong" />
    </header>
    <main class="text-center">
      <Songs :pallino="filterGener" />
      <Loader :is-loading="isLoading" />
    </main>
  </div>
</template>

<script>
import axios from "axios";

import Logo from "./components/Logo.vue";
import Songs from "./components/Songs.vue";
import Select from "./components/Select.vue";
import Loader from "./components/Loader.vue";
export default {
  name: "App",
  components: {
    Songs,
    Loader,
    Select,
    Logo,
  },
  data() {
    return {
      songs: [],
      isLoading: false,
      gener: "",
    };
  },
  computed: {
    filterGener() {
      if (!this.gener) return this.songs;

      return this.songs.filter((song) => song.genre.includes(this.gener));
    },
  },
  methods: {
    getSongs() {
      this.isLoading = true;
      axios
        .get("https://flynn.boolean.careers/exercises/api/array/music")
        .then((res) => {
          this.songs = res.data.response;
          this.isLoading = false;
        });
    },
    findSong(i) {
      this.gener = i;
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
  display: flex;
  justify-content: space-between;
}
main {
  height: 100%;
  background-color: $main-bg-color;
  color: white;
  padding: 50px 0;
}
</style>
