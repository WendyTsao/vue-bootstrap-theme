<template>
  <main id="main" class="site-main main">
    <section class="section">
      <div class="container">
        <div class="row">
          <section class="hero hero--xs w-100 pt-0">
            <div class="container">
              <h1 class="display-2 text-bold mb-3">
                Themes Built for Developers.
              </h1>
              <h5 class="text-gray-soft text-regular">
                Component-based frameworks designed and built by the best
                Bootstrap creators in the world.
              </h5>
            </div>
          </section>
          <section class="section pt-3 official-themes-page pb-0">
            <div class="screenshots-masonry">
              <img
                class="d-none d-lg-block"
                src="https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/official-themes/theme-masonry.jpg"
              />
              <img
                class="d-block d-lg-none"
                src="https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/official-themes/theme-masonry-mobile.jpg"
              />
            </div>
            <div class="container">
              <div class="row align-items-center justify-content-center mb-1 mt-5 mb-md-5 text-center">
                <div class="col-md-3 col-6 mb-5 mb-md-0 border-right">
                  <h6 class="mb-1">Average Rating</h6>
                  <div class="d-flex align-items-center justify-content-center">
                    <ul class="rating d-inline mb-0 mr-2">
                      <li class="rating__item rating__item--active"></li>
                      <li class="rating__item rating__item--active"></li>
                      <li class="rating__item rating__item--active"></li>
                      <li class="rating__item rating__item--active"></li>
                      <li class="rating__item rating__item--active"></li>
                    </ul>
                    <p class="fs-13 text-gray-soft d-inline">4.9/5</p>
                  </div>
                </div>
                <div class="col-md-3 col-6 mb-5 mb-md-0 border-right">
                  <h6 class="mb-1">Our Guarantee</h6>
                  <p class="fs-13 text-gray-soft">100% money back.</p>
                </div>
                <div class="col-md-3 col-6 mb-5 mb-md-0 border-right">
                  <h6 class="mb-1">Free Updates</h6>
                  <p class="fs-13 text-gray-soft">Never pay for an update.</p>
                </div>
                <div class="col-md-3 col-6 mb-5 mb-md-0">
                  <h6 class="mb-1">Free Support</h6>
                  <p class="fs-13 text-gray-soft">6 months included</p>
                </div>
              </div>

              <div class="row align-items-center justify-content-between py-4">
                <div class="col-xl-5 col-lg-6 pt-4">
                  <h1 class="mb-2 text-bold w-75">
                    Built as frameworks from the ground up.
                  </h1>
                  <p class="fs-16 text-gray-soft">
                    Each theme is architected as an extension of Bootstrap,
                    built for a specific set of problems. This means not only
                    extending the base components of Bootstrap, but also adding
                    completely new components, utilities, and plugins.
                  </p>
                </div>
                <div class="col-lg-12 mb-5">
                  <img
                    class="img-fluid mx-auto framework-progression-graphic d-none d-lg-block"
                    src="https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/official-themes/framework-progression.png"
                    alt=""
                  />
                  <img
                    class="img-fluid mx-auto framework-progression-graphic d-block d-lg-none"
                    src="https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/official-themes/framework-progression-mobile.jpg"
                    alt=""
                  />
                </div>
              </div>

              <div class="row align-items-center justify-content-between">
                <div class="col-lg-6 mt-5 order-2 order-lg-1">
                  <img
                    class="img-fluid mx-auto d-block"
                    src="https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/official-themes/review-process.svg"
                    alt=""
                  />
                </div>
                <div class="col-lg-5 order-1 order-lg-2">
                  <h1 class="mb-2 text-bold w-75">
                    Every theme gets reviewed by us.
                  </h1>
                  <p class="fs-16 text-gray-soft">
                    The Boostrap team reviews every new theme and update against
                    a set of guidelines we wrote. These cover tons of factors
                    including design, component flexibility, class naming,
                    directory structure, build tooling, plugin reusability…the
                    list goes on and on.
                  </p>
                </div>
              </div>

              <div
                class="row align-items-center justify-content-between mt-5 my-lg-5 pt-5"
              >
                <div class="col-lg-5 mb-3 mb-lg-5">
                  <h1 class="mb-2 text-bold w-75">
                    Build tools and full documention.
                  </h1>
                  <p class="fs-16 text-gray-soft">
                    Components, plugins, and build tools are all thoroughly
                    documented with live examples and markup for easier use and
                    customization—just like Bootstrap itself. Not comfortable
                    diving that deep? No worries, you just use the compiled CSS
                    and examples pages!
                  </p>
                  <a
                    class="btn btn-brand"
                    href="https://bootstrap-themes.github.io/dashboard/docs/"
                    >Explore the Dashboard docs</a
                  >
                </div>
                <div class="col-lg-6 mb-4 mt-4">
                  <img
                    class="img-fluid mx-auto d-block"
                    src="https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/official-themes/terminal.jpg"
                    alt=""
                  />
                </div>
              </div>

              <div class="row align-items-center justify-content-between mb-5 pt-5 mb-lg-3 text-center">
                <div class="col-sm-4 px-sm-4 pb-5" v-for="icontext in ThemesIconCard" :key="icontext.imgUrl">
                  <IconCard :content="icontext"></IconCard>
                </div>
              </div>
            </div>
          </section>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import IconCard from "../components/IconCard.vue";
export default {
  components: { IconCard },
  setup() {
    const ThemesIconCard = [
      {
        imgUrl:
          "https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/official-themes/components-icon.svg",
        title: "Components and examples",
        text:
          "Each theme features new components built to match Bootstrap's level ofquality and re-usability.",
      },
      {
        imgUrl:
          "https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/official-themes/sliders-icon.svg",
        title: "Tons of variables",
        text:
          "Themes inherit their style from custom variables, like Bootstrap, so basic customization is easy.",
      },
      {
        imgUrl:
          "https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/official-themes/wrenches-icon.svg",
        title: "Source files",
        text:
          "Each theme includes all the source and compiled files, making deep customization possible.",
      },
    ];
    return { starrate, ThemesIconCard };
  },
};
</script>

<style>
</style>