<script>
import HeaderApp from './components/HeaderApp.vue';
import JumbotronApp from './components/JumbotronApp.vue';
import SeriesApp from './components/SeriesApp.vue';
import ProductsApp from './components/ProductsApp.vue';
import FooterApp from './components/FooterApp.vue';
export default {

  components: {
    HeaderApp,
    JumbotronApp,
    ProductsApp,
    FooterApp,
    SeriesApp,
  },

  data() {
    return {

    }
  },
  methods: {},
}

</script>

<template>
  <div class="container">

    <HeaderApp />
    <JumbotronApp />
    <SeriesApp />
    <ProductsApp />
    <FooterApp />

  </div>
</template>

<style lang="scss">
@use './style/general.scss';
@use './style/partials/variables' as *;
@use './style/partials/mixins' as *;

.container {
  height: 100vh;
  width: 100%;
  margin: 0 auto;
  background-color: $white_color;
}
</style>
