<template>
  <div>
    <h2>{{ name }}</h2>
    <button @click="changeName">Change Name</button>
    <h2>{{ count }}</h2>
    <button @click="increase(5)">Increase 5</button>
    <button @click="increase()">+</button>
    <button @click="decrease()">-</button>
    <button @click="increase(-5)">Decrease 5</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "Marcel",
      count: 0,
    };
  },
  methods: {
    changeName(event) {
      console.log(event);
      return (this.name = "Batman");
    },
    increase(num = 1) {
      return (this.count += num);
    },
    decrease(num = 1) {
      return (this.count -= num);
    },
  },
};
</script>

<style>
</style>