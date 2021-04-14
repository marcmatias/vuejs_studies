<template>
  <div id="index">
    <h1 id="title">Index</h1>

    <!-- Components -->
    <!-- <HelloWorld /> -->
    <!-- <ConditionalExample /> -->
    <!-- <ListExample /> -->
    <!-- <ListConditionalExample /> -->
    <!-- <Methods /> -->
    <!-- <EventHandling /> -->
    <Computed />
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
// import ConditionalExample from "./components/ConditionalExamples.vue";
// import ListExample from "./components/ListExample.vue";
// import ListConditionalExample from "./components/ListConditionalExample.vue";
// import Methods from "./components/Methods.vue";
// import EventHandling from "./components/EventHandling.vue";
import Computed from "./components/Computed.vue";

export default {
  name: "App",
  components: {
    // HelloWorld
    // ConditionalExample,
    // ListConditionalExample,
    // Methods,
    // EventHandling,
    Computed,
  },
};
</script>

<style>
body {
  background-color: rgb(17, 17, 17);
}
#index {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: rgb(241, 241, 241);
  margin-top: 60px;
}
#title {
  margin-bottom: 60px;
}
</style>
