<script>
import PokemonsList from './pokemons/PokemonsList.vue';
import AppHeader from './AppHeader.vue';
export default {
    name: 'AppMain',
    components: { PokemonsList, AppHeader }
};
</script>

<template>
    <main class="container">
        <section class="pokedex shadow">

            <AppHeader @type-change="filterPokemon" />

            <div class="pokemon-container">
                <PokemonsList />
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
.pokedex {
    height: 700px;
    background-color: lightgray;
    border-radius: 40px;
    border: 2px solid black;
}

.pokemon-container {
    margin: 30px;
    background-color: rgb(29, 29, 29);
    height: 80%;
    border-radius: 40px;
}
</style>