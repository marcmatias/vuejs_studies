<template>
  <div>
    <h2 v-if="num === 0">The number is zero</h2>
    <h2 v-else-if="num > 0">The number is positive</h2>
    <h2 v-else-if="num < 0">The number is negative</h2>
    <h2 v-else>Not a number</h2>
    <h2 v-show="display === true">v-show</h2>
    <h2 v-if="display === true">v-if</h2>
  </div>
  <template v-if="display === true">
    <h2>@marcmatias</h2>
    <h2>Example</h2>
    <h2>Hide elements</h2>
  </template>
</template>

<script>
export default {
  data() {
    return {
      num: "Hello",
      display: true,
    };
  },
};
</script>

<style>
</style>