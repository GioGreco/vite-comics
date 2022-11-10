<template>
  <HeaderComponent/>
  <main>
    <h3 class="container">-- Content Goes Here --</h3>
  </main>
  <BrowseSectionsComponent/>
  <FooterComponent/>
</template>

<script>
  import HeaderComponent from './components/HeaderComponent.vue';
  import FooterComponent from './components/FooterComponent.vue';
  import BrowseSectionsComponent from './components/BrowseSectionsComponent.vue';

  export default {
    components: {
      HeaderComponent,
      FooterComponent,
      BrowseSectionsComponent
    }
  }
</script>

<style lang="scss" scoped>
main{
  background-color: black;
  height: 100px;
  color: white;
  line-height: 100px;
}
</style>