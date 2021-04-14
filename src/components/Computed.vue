<template>
  <div>
    <h2>Fullname - {{ firstName }} {{ lastName }}</h2>
    <h2>Computed Fullname - {{ fullName }}</h2>
  </div>
</template>

<script>
export default {
  data() {
    return {
      firstName: "Bruce",
      lastName: "Wayne",
    };
  },
  methods: {},
  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName}`;
    },
  },
};
</script>

<style>
</style>