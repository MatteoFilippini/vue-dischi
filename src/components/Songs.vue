<template>
  <div>
    <div class="container">
      <div class="row">
        <div class="col-2 p-2" v-for="(song, index) in songs" :key="index">
          <SongCard :song="song" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SongCard from "./SongCard.vue";
export default {
  name: "Songs",
  props: ["songs"],
  components: {
    SongCard,
  },
};
</script>

<style lang="scss" scoped>
</style>