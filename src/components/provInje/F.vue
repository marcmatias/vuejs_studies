<template>
  <div>
    <h2>{{ username }}</h2>
    <h2>{{ lastname }}</h2>
  </div>
</template>

<script>
export default {
  name: "F",
  inject: ["username", "lastname"],
};
</script>