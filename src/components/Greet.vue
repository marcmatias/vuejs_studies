<template>
  <h2>{{ name }} {{ lastName }}</h2>
</template>

<script>
export default {
  name: "Greet",
  props: ["name", "lastName"],
};
</script>

<style scoped>
</style>