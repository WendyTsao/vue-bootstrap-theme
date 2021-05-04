<template>
  <img :src="content.imgUrl" />
  <h5 class="my-2 text-bold">{{content.title}}</h5>
  <p class="text-gray-soft">{{content.text}}
  </p>
</template>

<script>
export default {
  props: {
    content: {
      imgUrl:
        "https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/official-themes/components-icon.svg",
      title: "Components and examples",
      text: "Each theme features new components built to match Bootstrap's level ofquality and re-usability.",
    },
  },
};
</script>

<style>
</style>