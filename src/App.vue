<template>
  <div id="index">
    <h1 id="title">Index</h1>
    <!-- <input type="text" v-model="inputtext"> -->
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
    <!-- <C /> -->
    <!-- <Greet name="Hero" last-name="Link" />
    <Greet name="Princess" last-name="Zelda" />
    <Greet :name="firstName" :last-name="lastName" /> -->
    <!-- <Article id="article" title="Article Title" :is-published="true" /> -->
    <!-- <button @click="showPopup = true">ShowPopup</button> -->
    <!-- <Popup v-show="showPopup" @close="closePopup"/> -->
    <Input v-model="name" />
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
// import Greet from "./components/Greet.vue";
// import C from "./components/provInje/C.vue";
// import Article from "./components/Article.vue";
// import Popup from "./components/Popup.vue"
import Input from "./components/Input.vue";
export default {
  name: "App",
  data() {
    return {
      name: "",
      inputtext: "",
      firstName: "Marcel",
      lastName: "Marques",
      showPopup: false,
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
    // Greet,
    // C, //Provide, Inject example
    // Article,
    // Popup,
    Input,
  },
  methods: {
    closePopup(name) {
      this.showPopup = false;
      console.log(name);
    },
  },
  provide() {
    return {
      username: "Marcel",
      lastname: this.lastName,
    };
  },
};
</script>

<style>
#index {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}
#title {
  margin-bottom: 60px;
}
</style>
