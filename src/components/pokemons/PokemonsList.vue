<script>
import axios from 'axios';
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons'

export default {
    name: 'PokemonsList',
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
    <section id="pokemons"></section>
</template>

<style lang="scss"></style>