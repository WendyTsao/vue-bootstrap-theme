<template>
  <div class="theme-card">
    <div class="theme-card__body">
      <a
        class="d-block"
        href="https://themes.getbootstrap.com/product/craft-bootstrap-5-admin-dashboard-theme/"
      >
        <img :src="content.imgUrl" />
      </a>

      <a
        class="theme-card__body__overlay btn btn-brand btn-sm"
        target="_blank"
        :href="content.livepreviewUrl"
        >Live preview</a
      >
    </div>
    <div class="theme-card__footer">
      <div class="theme-card__footer__item">
        <a
          class="theme-card__title mr-1"
          href="https://themes.getbootstrap.com/product/craft-bootstrap-5-admin-dashboard-theme/"
          >{{ content.title }}</a
        >
        <p class="theme-card__info"></p>
        <ul class="prod_cats_list">
          <li>
            <a
              href="https://themes.getbootstrap.com/product-category/admin-dashboard/"
              >{{ content.subtitle }}</a
            >
          </li>
        </ul>
        <p></p>
      </div>
      <div class="theme-card__footer__item">
        <p class="theme-card__price">
          <span class="woocommerce-Price-amount amount"
            ><span class="woocommerce-Price-currencySymbol">$</span
            >{{ content.price }}</span
          >
        </p>
        <ul class="rating">
          <li v-for="i in 5" :class="['rating__item',{ 'rating__item--active': content.starrate >= i }]" :key="i"></li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    content: {
      type: Object,
      default: {
        imgUrl: "",
        livepreviewUrl: "",
        title: "",
        subtitle: "",
        price: "",
        starrate: 0,
      },
    },
  },
};
</script>

<style>
</style>