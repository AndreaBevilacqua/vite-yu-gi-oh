<script>
export default {
    name: 'AppMain'
};
</script>

<template>
    <main class="container">
        <section class="pokedex">
            <div class="pokedex-buttons d-flex gap-4 p-4">
                <button type="button" class="btn btn-primary btn-lg"> </button>
                <button type="button" class="btn btn-danger"></button>
                <button type="button" class="btn btn-warning"></button>
                <button type="button" class="btn btn-success"></button>
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
.pokedex {
    height: 600px;
    background-color: lightgray;
    border-radius: 40px;
}

.pokedex-buttons {
    background-color: grey;
    width: 18%;
    border-radius: 40px 0 40px 0;
    margin-bottom: 20px;
}
</style>