<script>
export default {
    name: 'PokemonCard',
    props: {
        name: String,
        image: String,
        number: Number,
        type: String,
    }
}
</script>

<template>
    <div class="pokemon-card text-center p-2 text-white">
        <img :src="image" :alt="name" class="img-fluid mb-3">
        <div>{{ number }}</div>
        <h3 class="fs-5">{{ name }}</h3>
        <div>{{ type }}</div>
    </div>
</template>

<style lang="scss">
.pokemon-card {
    background-color: rgb(194, 194, 194);
    border-radius: 20px;

    img {
        border-radius: 20px;
        height: 135px;
        width: 135px;
    }
}
</style>