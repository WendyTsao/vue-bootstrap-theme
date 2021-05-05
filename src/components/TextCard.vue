<template>
  <div class="col-md-3 col-6 mb-5 mb-md-0">
    <h6 class="mb-1">{{ content.title }}</h6>
    <div class="d-flex align-items-center justify-content-center">
      <slot></slot>
      <p class="fs-13 text-gray-soft">{{ content.text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    content: {
      type: Object,
      default: {
        title: "",
        text: "",
      },
    },
  },
  setup() {},
};
</script>

<style>
</style>