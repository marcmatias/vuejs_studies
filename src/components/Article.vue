<template>
  <div>
    <h2 v-bind="$attrs">{{ title }} {{ likes }}</h2>
    <h2>{{ isPublished ? "Yes" : "No" }}</h2>
  </div>
</template>

<script>
export default {
  name: "Article",
  props: {
    title: {
      type: String,
      required: true,
    },
    likes: {
      type: Number,
      default: 0,
    },
    isPublished: Boolean,
  },
  inheritAttrs: false,
};
</script>