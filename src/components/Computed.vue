<template>
  <div>
    <h2>Fullname - {{ firstName }} {{ lastName }}</h2>
    <h2>Computed Fullname - {{ fullName }}</h2>
    <h2>Method Total - {{ getTotal() }}</h2>
    <button @click="items.push({ id: 4, title: 'keyboard', price: 500 })">
      Add Item
    </button>
    <h2>
      Total -
      {{ items.reduce((total, curr) => (total = total + curr.price), 0) }}
    </h2>
    <h2>Computed Total - {{ total }}</h2>
    <input type="text" v-model="country" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      firstName: "Bruce",
      lastName: "Wayne",
      items: [
        {
          id: 1,
          title: "TV",
          price: 199,
        },
        {
          id: 2,
          title: "PC",
          price: 299,
        },
        {
          id: 3,
          title: "Smartphone",
          price: 399,
        },
      ],
      country: "",
    };
  },
  methods: {
    getTotal() {
      console.log("getTotal Method");
      return this.items.reduce(
        (total, curr) => (total = total + curr.price),
        0
      );
    },
  },
  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName}`;
    },
    total() {
      console.log("Computed Total");
      return this.items.reduce(
        (total, curr) => (total = total + curr.price),
        0
      );
    },
  },
};
</script>

<style>
</style>