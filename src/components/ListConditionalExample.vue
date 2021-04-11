<template>
  <div>
    <h2 v-for="name in names" :key="name">
      <div v-if="name === 'Bruce'">
        {{ name }}
      </div>
    </h2>
  </div>
</template>

<script>
export default {
  data() {
    return {
      names: ["Bruce", "Diana", "Clark"],
    };
  },
};
</script>

<style>
</style>