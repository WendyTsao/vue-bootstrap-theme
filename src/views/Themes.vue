<template>
  <main id="main" class="site-main main over-hidden">
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
              <img class="d-none d-lg-block"
                src="https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/official-themes/theme-masonry.jpg" />
              <img class="d-block d-lg-none"
                src="https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/official-themes/theme-masonry-mobile.jpg" />
            </div>
            <div class="container">
              <div class="row align-items-center justify-content-center mb-1 mt-5 mb-md-5 text-center">
                    <TextCard v-for="(card, index) in ThemesTextCard" 
                    :class="{'border-right': index < ThemesTextCard.length - 1}" 
                    :content="card" :key="card.title">
                        <ul v-if="card.hasStarrate" class="rating d-inline mb-0 mr-2">
                            <li v-for="i in 5" class="rating__item rating__item--active" :key="i"> 
                            </li>
                        </ul>
                    </TextCard>
              </div>

             <div v-for="(graphic, index) in ThemesGraphicArea" 
                  :class="['row align-items-center justify-content-between py-4', 
                  {'flex-row-reverse': index % 2 === 1}]"
                  :key="graphic.imgUrl">
                <Text :title="graphic.title" :text="graphic.text">
                  <a v-if="graphic.hasButton" class="btn btn-brand" href="https://bootstrap-themes.github.io/dashboard/docs/">
                      Explore the Dashboard docs
                  </a>
                </Text>

                <Image :class="index === 0 ? 'col-lg-12':'col-lg-6'"
                      :imgUrl="graphic.imgUrl" 
                      :mobileImgUrl="graphic.mobileImgUrl"></Image>
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
import Text from '../components/Text.vue';
import Image from '../components/Image.vue';

export default {
  components: { TextCard, IconCard, Text, Image },
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
        imgUrl: "https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/official-themes/components-icon.svg",
        title: "Components and examples",
        text: "Each theme features new components built to match Bootstrap's level ofquality and re-usability.",
      },
      {
        imgUrl: "https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/official-themes/sliders-icon.svg",
        title: "Tons of variables",
        text: "Themes inherit their style from custom variables, like Bootstrap, so basic customization is easy.",
      },
      {
        imgUrl: "https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/official-themes/wrenches-icon.svg",
        title: "Source files",
        text: "Each theme includes all the source and compiled files, making deep customization possible.",
      },
    ];
    const ThemesGraphicArea = [
      {
        title: "Built as frameworks from the ground up.",
        text: "Each theme is architected as an extension of Bootstrap, built for a specific set of problems. This means not only extending the base components of Bootstrap, but also adding completely new components, utilities, and plugins.",
        imgUrl:"https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/official-themes/framework-progression.png",
        mobileImgUrl:"https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/official-themes/framework-progression-mobile.jpg",
      },
      {
        title: "Every theme gets reviewed by us.",
        text: "The Boostrap team reviews every new theme and update against a set of guidelines we wrote. These cover tons of factors including design, component flexibility, class naming, directory structure, build tooling, plugin reusability…the list goes on and on.",
        imgUrl: "https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/official-themes/review-process.svg",
      },
      {
        title: "Build tools and full documention.",
        text: "Components, plugins, and build tools are all thoroughly documented with live examples and markup for easier use and customization—just like Bootstrap itself. Not comfortable diving that deep? No worries, you just use the compiled CSS and examples pages!",
        imgUrl: "https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/official-themes/terminal.jpg",
        hasButton: true,
      }
    ];

    return { ThemesTextCard, ThemesIconCard, ThemesGraphicArea };
  },
};
</script>

<style scoped>
    .over-hidden{
        overflow: hidden;
    }
</style>