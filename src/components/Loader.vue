<template>
  <div v-if="isLoading">Loading...</div>
</template>

<script>
export default {
  name: "Loader",
  props: ["isLoading"],
};
</script>

<style>
</style>