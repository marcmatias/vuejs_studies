<template>
  <h2>computed fullname - {{ fullName }}</h2>
  <button @click="changeFullName">Change fullname - {{ fullName }}</button>
</template>

<script>
export default {
  name: "SetterComputed",
  data() {
    return {
      firstName: "Bruce",
      lastName: "Wayne",
    };
  },
  methods: {
    changeFullName() {
      this.fullName = "Clark Kent";
    },
  },
  computed: {
    fullName: {
      get() {
        return `${this.firstName} ${this.lastName}`;
      },
      set(value) {
        const names = value.split(" ");
        this.firstName = names[0];
        this.lastName = names[1];
      },
    },
  },
};
</script>

<style>
</style>