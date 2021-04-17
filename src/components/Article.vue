<template>
  <h2>{{ title }} {{ likes }} {{ isPublished ? "Yes" : "No" }}</h2>
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
};
</script>