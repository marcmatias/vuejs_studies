<template>
  <div id="index">
    <h1 id="title">Index</h1>

    <!-- Components -->
    <!-- <HelloWorld /> -->
    <!-- <ConditionalExample /> -->
    <ListExample />
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
// import ConditionalExample from "./components/ConditionalExamples.vue";
import ListExample from "./components/ListExample.vue";

export default {
  name: "App",
  components: {
    // HelloWorld
    // ConditionalExample,
    ListExample,
  },
};
</script>

<style>
#index {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#title {
  margin-bottom: 60px;
}
</style>
