<template>
  <h2>{{ 2 + 2 }}</h2>
  <h2>Add method result: {{ add(2, 3, 5) }}</h2>
  <h2>Multiply method result: {{ multiply(base) }}</h2>
</template>

<script>
export default {
  data() {
    return {
      baseMultiplier: 15,
      base: 2,
    };
  },
  methods: {
    add(a, b, c) {
      return a + b + c;
    },
    multiply(num) {
      return num * this.baseMultiplier;
    },
  },
};
</script>

<style>
</style>