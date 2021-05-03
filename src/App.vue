<template>
  <Navigation></Navigation>
  <router-view></router-view>
  <Footer></Footer>
</template>

<script>
import Footer from "./components/Footer";
import Navigation from "./components/Navigation";

export default {
  components:{
    Footer, Navigation
  }
}
</script>

<style>

</style>