<template>
  <div>
    <div class="mt-4 mb-4">
      <img v-if="mobileImgUrl" class="img-fluid mx-auto d-block d-lg-none" :src="mobileImgUrl" />
      <img
        class="img-fluid mx-auto"
        :class="{ 'd-none d-lg-block': mobileImgUrl }"
        :src="imgUrl"
      />
    </div>
  </div>
</template>

<script>
export default {
  props: {
    imgUrl: { type: String },
    mobileImgUrl: { type: String },
  },
};
</script>

<style>
</style>