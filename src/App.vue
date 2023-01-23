<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import series from './data/series.js'
export default {
  nome: 'vite-comics',
  components: { AppHeader, AppMain, AppFooter },
  data() {
    return {
      series
    }
  }
}
</script>

<template>
  <app-header></app-header>
  <app-main :series="series"></app-main>
  <app-footer></app-footer>
</template>

<style lang="scss">
@use './assets/scss/style.scss';
</style>