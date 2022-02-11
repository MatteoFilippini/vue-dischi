<template>
  <select class="form-select me-3">
    <!-- <option selected>Open this select menu</option> -->
    <option value="1">One</option>
    <option value="2">Two</option>
    <option value="3">Three</option>
  </select>
</template>

<script>
export default {
  name: "Select",
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