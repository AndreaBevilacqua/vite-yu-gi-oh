<script>
import axios from 'axios';
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons'
import AppMain from './components/AppMain.vue';
export default {
  name: 'Pokemon',
  components: { AppMain },
  data: () => ({
    pokemons: []
  }),
  created() {
    axios.get(endpoint).then(res => {
      this.pokemons = res.data.docs;
    })
  }
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





