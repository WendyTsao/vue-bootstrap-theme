<template>
  <div class="col-sm-4 px-sm-4 pb-5">
    <img :src="content.imgUrl" />
    <h5 class="my-2 text-bold">{{ content.title }}</h5>
    <p class="text-gray-soft">{{ content.text }}</p>
  </div>
</template>

<script>
export default {
  props: {
    content: {
      type: Object,
      default: {
        imgUrl: "",
        title: "",
        text: "",
      },
    },
  },
};
</script>

<style>
</style>