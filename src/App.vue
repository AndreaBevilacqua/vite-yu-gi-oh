<script>
import AppMain from './components/AppMain.vue';
export default {
  name: 'Pokemon',
  components: { AppMain }
};
</script>

<template>
  <header>
    <h1 class="text-center m-5 text-white">POKÈDEX</h1>
  </header>
  <AppMain />
</template>

<style lang="scss">
@use './assets/scss/style.scss';
</style>





