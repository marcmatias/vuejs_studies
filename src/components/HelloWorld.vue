<template>
  <div>{{ greet }} {{ name }}</div>
  <div v-html="lastName"></div>
  <div v-text="nickName"></div>
  <div v-html="webpage"></div>
  <h2 :id="headingId">Heading</h2>
  <button :disabled="isDisabled">Button</button>
  <h2 class="underline">Underline text</h2>
  <h2 :class="status">Status</h2>
  <h2 :class="isSoldout ? 'success' : 'danger'">Sold Out</h2>
  <h2 :class="[isPromoted && 'promoted', isSoldout ? 'success' : 'danger']">
    Is Promoted
  </h2>
  <h2
    :class="{
      promoted: isPromoted,
      success: isSoldout,
      danger: !isSouldOut,
    }"
  >
    Object Conditional
  </h2>
  <h2 :style="styleObj">Style Obj</h2>
  <h2 :style="[styleObj, styleObjBg]">Style Objects</h2>
</template>


<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      greet: "Hello",
      name: "Marcel",
      lastName: "<b>Marques</b>",
      nickName: "@marcmatias",
      webpage: `<a href='https://marcmatias.github.io'>marcmatias.github.io</a>`,
      headingId: "heading",
      isDisabled: true,
      status: "success",
      isSoldout: false,
      isPromoted: true,
      styleObj: {
        "font-size": "35px",
        color: "lightgray",
        fontStyle: "italic",
      },
      styleObjBg: {
        "background-color": "gray",
        padding: "25px",
        "margin-left": "100px",
        "margin-right": "100px",
      },
    };
  },
};
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.underline {
  text-decoration: underline;
}
.danger {
  color: red;
}
.success {
  color: blue;
}
.promoted {
  font-style: italic;
}
</style>