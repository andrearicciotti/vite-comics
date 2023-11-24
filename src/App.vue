<script>
import HeaderApp from './components/HeaderApp.vue';
import ContentApp from './components/ContentApp.vue';
import ProductsApp from './components/ProductsApp.vue';
export default {

  components: {
    HeaderApp,
    ContentApp,
    ProductsApp,
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
    <ContentApp />
    <ProductsApp />
    
  </div>
</template>

<style lang="scss">
@use './style/general.scss';
@use './style/partials/variables' as *;
@use './style/partials/mixins' as *;

.container {
    margin: 0 auto;
    background-color: $white_color;
}
</style>
