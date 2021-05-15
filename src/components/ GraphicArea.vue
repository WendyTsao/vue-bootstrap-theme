<template>
  <div class="row align-items-center justify-content-between py-4">
    <div class="col-lg-5">
      <h1 class="mb-2 text-bold w-75">
        {{ content.title }}
      </h1>
      <p class="fs-16 text-gray-soft">
        {{ content.text }}
      </p>
      <slot></slot>
    </div>
    <div v-if="content.mobileImgUrl" class="mt-4 mb-4">
      <img class="img-fluid mx-auto d-block d-lg-none" :src="content.mobileImgUrl" />
    </div>
    <div :class="[content.imgClass,'mt-4','mb-4']">
      <img class="img-fluid mx-auto" 
      :class="{'d-none d-lg-block': content.mobileImgUrl}" 
      :src="content.imgUrl" />
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
        imgUrl: "",
        imgClass:"",
        mobileImgUrl: "",
      },
    },
  }
};
</script>

<style>
</style>