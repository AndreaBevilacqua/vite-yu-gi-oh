<script>
import axios from 'axios';
const endpoint = 'https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons'
import PokemonCard from './PokemonCard.vue';

export default {
    name: 'PokemonsList',
    data: () => ({
        pokemons: []
    }),
    components: { PokemonCard },
    created() {
        axios.get(endpoint).then(res => {
            this.pokemons = res.data.docs;
        })
    }
};
</script>

<template>
    <section id="pokemons" class="my-5 p-3 overflow-auto">
        <div class="row g-4 row-cols-lg-5">
            <div class="col" v-for="pokemon in pokemons" :key="pokemon._id">
                <PokemonCard :name="pokemon.name" :image="pokemon.imageUrl" :number="pokemon.number"
                    :type="pokemon.type1" />
            </div>
        </div>
    </section>
</template>

<style lang="scss"></style>