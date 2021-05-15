<template>
    <div class="col-lg-5">
      <h1 class="mb-2 text-bold w-75">
        {{ title }}
      </h1>
      <p class="fs-16 text-gray-soft">
        {{ text }}
      </p>
      <slot></slot>
    </div>
</template>

<script>

export default {
   props:{
        title:{type:String},
        text:{type:String},
    }
};
</script>

<style>
</style>