<template>
  <div>
    <h2>This is a popup</h2>
    <input type="text" v-model="name" />
    <button @click="$emit('close', name)">Close</button>
  </div>
</template>

<script>
export default {
  name: "Popup",
  emits: {
    close: (name) => {
      return !name ? false : true;
    },
  },
  data() {
    return {
      name: "",
    };
  },
};
</script>