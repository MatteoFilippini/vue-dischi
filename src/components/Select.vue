<template>
  <select
    class="form-select me-3"
    @change="$emit('genere', valueSelect)"
    v-model="valueSelect"
  >
    <option value="">Tutti i generi</option>
    <option
      :value="uno.genre"
      v-for="(uno, index) in pincopallino"
      :key="index"
    >
      {{ uno.genre }}
    </option>
  </select>
</template>

<script>
export default {
  name: "Select",
  props: ["pincopallino"],
  data() {
    return {
      valueSelect: "",
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/-var.scss";

select {
  width: 25%;
  background-color: $main-bg-color;
  color: white;
}
</style>