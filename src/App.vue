<script>
import axios from 'axios';
import { store } from './data/store';
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons'
import AppMain from './components/AppMain.vue';


export default {
  name: 'Pokemon',
  components: { AppMain },
  data: () => ({
    pokemons: []
  }),
  methods: {
    fetchPokemon() {
      axios.get(endpoint).then(res => {
        store.pokemons = res.data.docs;
      })
    },
    fetchTypes() {
      axios.get(endpoint + '/types1').then(res => {
        store.types = res.data.map((type, i) => {
          return {
            id: i + 1,
            label: type,
            value: type,
          }
        })
      })
    },
    filterPokemon(type) {
      const url = `${endpoint}?eq[type1]=${type}`;
      this.fetchPokemon(url);
    }
  },
  created() {
    this.fetchPokemon();
    this.fetchTypes();
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





