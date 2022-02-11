<template>
  <select class="form-select me-3">
    <option :value="index" v-for="(song, index) in songs" :key="index">
      {{ song.genre }}
    </option>
  </select>
</template>

<script>
export default {
  name: "Select",
  props: ["songs"],
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/-var.scss";

select {
  width: 100px;
  background-color: $main-bg-color;
  color: white;
}
</style>