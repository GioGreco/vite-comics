<template>
  <HeaderComponent/>
  <Jumbotron/>
  <CurrentSeriesComponent/>
  <BrowseSectionsComponent/>
  <FooterComponent/>
</template>

<script>
  import HeaderComponent from './components/HeaderComponent.vue';
  import FooterComponent from './components/FooterComponent.vue';
  import BrowseSectionsComponent from './components/BrowseSectionsComponent.vue';
  import Jumbotron from './components/Jumbotron.vue';
  import CurrentSeriesComponent from './components/CurrentSeriesComponent.vue';

  export default {
    components: {
      HeaderComponent,
      FooterComponent,
      BrowseSectionsComponent,
      Jumbotron,
      CurrentSeriesComponent
    }
  }
</script>

<style lang="scss" scoped>

</style>