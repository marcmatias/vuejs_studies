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
    <!-- <Computed /> -->
    <!-- <SetterComputed /> -->
    <!-- <Watcher /> -->
    <C />
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
// import ConditionalExample from "./components/ConditionalExamples.vue";
// import ListExample from "./components/ListExample.vue";
// import ListConditionalExample from "./components/ListConditionalExample.vue";
// import Methods from "./components/Methods.vue";
// import EventHandling from "./components/EventHandling.vue";
// import Computed from "./components/Computed.vue";
// import SetterComputed from "./components/SetterComputed.vue";
// import Watcher from "./components/Watcher.vue";
import C from "./components/provInje/C.vue";

export default {
  name: "App",
  data() {
    return {
      lastname: "Marques",
    };
  },
  components: {
    // HelloWorld
    // ConditionalExample,
    // ListConditionalExample,
    // Methods,
    // EventHandling,
    // Computed,
    // SetterComputed,
    // Watcher,
    C,
  },
  provide() {
    return {
      username: "Marcel",
      lastname: this.lastname,
    };
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
