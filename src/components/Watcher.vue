<template>
  <h2>Volume Tracker (0-20)</h2>
  <h3>Current Volume - {{ volume }}</h3>
  <div>
    <button @click="volume += 2">Increase</button>
    <button @click="volume -= 2">Decrese</button>
    <input type="text" v-model="movie" />
    <input type="text" v-model="movieInfo.title" />
    <input type="text" v-model="movieInfo.actor" />
  </div>
</template>

<script>
export default {
  name: "Watcher",
  data() {
    return {
      volume: 0,
      movie: "Batman",
      movieInfo: {
        title: "",
        actor: "",
      },
    };
  },
  methods: {},
  computed: {},
  watch: {
    volume(newValue, oldValue) {
      if (newValue > oldValue && newValue == 16) {
        alert(
          "Listening to a high volume for a long time may damage your hearing"
        );
      }
    },
    movie: {
      handler(newValue) {
        console.log(
          `Calling API with movie name = ${newValue.title} and actor = ${newValue.actor}`
        );
      },
      immediate: true,
    },
    movieInfo: {
      handler(newValue) {
        console.log(`Calling API with movie with title = ${newValue}`);
      },
      deep: true,
    },
  },
};
</script>

<style>
</style>