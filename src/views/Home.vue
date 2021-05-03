<template>
  <!-- main -->
  <main id="main" class="site-main main">
    <section class="hero">
      <!-- Large header banner -->
      <div class="container">
        <img
          src="https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/elements/bootstrap-stack.png"
          srcset="
            https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/elements/bootstrap-stack.png    1x,
            https://themes.getbootstrap.com/wp-content/themes/bootstrap-marketplace/assets/images/elements/bootstrap-stack@2x.png 2x
          "
        />
        <h1 class="display-1 text-bold">Build anything</h1>
        <h5 class="text-gray-soft text-regular">
          Themes built by or reviewed by Bootstrap's creators.
        </h5>
        <a
          class="button button-brand btn-lg mb-5 mb-lg-2"
          href="https://themes.getbootstrap.com/official-themes"
          >Why our themes?</a
        >
      </div>
    </section>
    <section class="section">
      <div class="container">
        <div class="theme-cards-holder">
          <div class="theme-cards__heading">
            <div>
              <h5 class="theme-cards__title">Latest</h5>
              <p class="text-gray-soft">
                Most recently added to our collection.
              </p>
            </div>
            <a
              class="theme-cards__heading__button btn btn-outline-brand btn-sm"
              href="https://themes.getbootstrap.com/shop/?orderby=date"
              >View all</a
            >
          </div>
          <ul class="row">
            <li class="col-6" v-for="theme in latestThemes" :key="theme.imgUrl">
              <ThemeCard :content="theme"></ThemeCard>
            </li>
          </ul>
          <a
            class="btn btn-brand btn-block d-md-none"
            href="https://themes.getbootstrap.com/shop/?orderby=date"
            >View all latest themes</a
          >
        </div>
        <div class="theme-cards-holder">
          <div class="theme-cards__heading">
            <div>
              <h5 class="theme-cards__title">Popular</h5>
              <p class="text-gray-soft">Top-sellers in the past week!</p>
            </div>
            <!-- Removed for now because we're listing all the themes directly on the homepage -->
            <!-- <a class="theme-cards__heading__button btn btn-outline-brand btn-sm" href="https://themes.getbootstrap.com/shop/?orderby=popularity">View all</a> -->
          </div>
          <ul class="row">
            <li class="col-6" v-for="theme in popularTheme" :key="theme.imgUrl">
              <ThemeCard :content="theme"></ThemeCard>
            </li>
          </ul>
          <!-- Removed for now because we're listing all the themes directly on the homepage -->
          <!-- <a class="btn btn-brand btn-block d-md-none mb-4" href="https://themes.getbootstrap.com/shop/?orderby=popularity">View all popular themes</a> -->
        </div>
      </div>
    </section>
  </main>
  <!-- main end -->
</template>

<script>
import ThemeCard from "../components/ThemeCard.vue";
// @ is an alias to /src

export default {
  components: { ThemeCard },
  setup() {
    const latestThemes = [
      {
        imgUrl:
          "https://themes.getbootstrap.com/wp-content/uploads/2021/03/thumbnail-540x405.png",
        livepreviewUrl:
          "https://themes.getbootstrap.com/preview/?theme_id=86954",
        title: "Craft – Bootstrap 5 Admin Dashboard Theme",
        subtitle: "Admin & Dashboard",
        price: "49.00",
        starrate: 0,
      },
      {
        imgUrl:
          "https://themes.getbootstrap.com/wp-content/uploads/2021/03/start-react-540x405.png",
        livepreviewUrl:
          "https://themes.getbootstrap.com/preview/?theme_id=86954",
        title: "Start – React Bootstrap 5 Admin Dashboard Theme",
        subtitle: "Admin & Dashboard",
        price: "49.00",
        starrate: 5,
      },
    ];

    const popularTheme = [
      {
        imgUrl:
          "https://themes.getbootstrap.com/wp-content/uploads/2019/03/v2.8.2-540x405.jpeg",
        livepreviewUrl:
          "https://themes.getbootstrap.com/product/falcon-admin-dashboard-webapp-template/",
        title: "Falcon – Admin Dashboard & WebApp Template",
        subtitle: "Admin & Dashboard",
        price: "49.00",
        starrate: 5,
      },
      {
        imgUrl:
          "https://themes.getbootstrap.com/wp-content/uploads/2019/04/landkit-screenshot-v2.0.0-540x405.jpg",
        livepreviewUrl:
          "https://themes.getbootstrap.com/product/landkit/",
        title: "Landkit – Multipurpose Template + UI Kit",
        subtitle: "Admin & Dashboard",
        price: "49.00",
        starrate: 5,
      },
    ];
    return { latestThemes, popularTheme };
  },
};
</script>
