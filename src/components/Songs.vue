<template>
  <div>
    <div class="container">
      <div class="row">
        <div class="col-2 p-2" v-for="(unpippo, index) in pallino" :key="index">
          <SongCard :matteo="unpippo" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SongCard from "./SongCard.vue";
export default {
  name: "Songs",
  props: ["pallino"],
  components: {
    SongCard,
  },
};
</script>

<style lang="scss" scoped>
</style>