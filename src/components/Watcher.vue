<template>
  <h2>Volume Tracker (0-20)</h2>
  <h3>Current Volume - {{ volume }}</h3>
  <div>
    <button @click="volume += 2">Increase</button>
    <button @click="volume -= 2">Decrese</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      volume: 0,
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
  },
};
</script>

<style>
</style>