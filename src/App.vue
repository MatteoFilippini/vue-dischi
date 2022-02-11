<template>
  <div>
    <header>
      <Logo />
      <Select :songs="songs" @genere="findSong" />
    </header>
    <main class="text-center">
      <Songs :songs="songs" />
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
  // computed: {
  //   filterGener() {
  //     return this.songs.filter((song) => {
  //       song.gener.includes(gener);
  //     });
  //   },
  // },
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
      console.log(i);
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
