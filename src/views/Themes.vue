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
                    <TextCard v-for="card in ThemesTextCard" :content="card" :key="card.title">
                        <ul v-if="card.hasStarrate" class="rating d-inline mb-0 mr-2">
                            <li v-for="i in 5" class="rating__item rating__item--active" :key="i"> 
                            </li>
                        </ul>
                    </TextCard>
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

              <div class="row align-items-center justify-content-between mt-5 my-lg-5 pt-5">
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
                  <IconCard :content="icontext" v-for="icontext in ThemesIconCard" :key="icontext.imgUrl" />
              </div>
            </div>
          </section>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import TextCard from "../components/TextCard.vue";
import IconCard from "../components/IconCard.vue";

export default {
  components: { TextCard, IconCard },
  setup() {
    const ThemesTextCard = [
      {
        title: "Average Rating",
        text: "4.9/5",
        hasStarrate: true
      },
      {
        title: "Our Guarantee",
        text: "100% money back.",
      },
      {
        title: "Free Updates",
        text: "Never pay for an update.",
      },
      {
        title: "Free Support",
        text: "6 months included",
      },
    ];
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
    return { ThemesTextCard, ThemesIconCard };
  },
};
</script>

<style>
</style>