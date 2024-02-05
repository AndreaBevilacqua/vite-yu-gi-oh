<script>
import { store } from '../../data/store';
import PokemonCard from './PokemonCard.vue';

export default {
    name: 'PokemonsList',
    data: () => ({
        store
    }),
    components: { PokemonCard }
};
</script>

<template>
    <section id="pokemons" class="my-5 p-3 overflow-auto">
        <div class="row g-4 row-cols-lg-5">
            <div class="col" v-for="pokemon in store.pokemons" :key="pokemon._id">
                <PokemonCard :name="pokemon.name" :image="pokemon.imageUrl" :number="pokemon.number"
                    :type="pokemon.type1" />
            </div>
        </div>
    </section>
</template>

<style lang="scss"></style>