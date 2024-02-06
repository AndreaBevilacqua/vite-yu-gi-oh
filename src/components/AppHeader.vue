<script>
export default {
    name: 'AppHeader'
}
</script>

<template>
    <div class="pokedex-header d-flex justify-content-between">
        <div class="pokedex-buttons d-flex gap-4 p-4">
            <button type="button" class="btn btn-primary btn-lg"> </button>
            <button type="button" class="btn btn-danger"></button>
            <button type="button" class="btn btn-warning"></button>
            <button type="button" class="btn btn-success"></button>
        </div>
        <div class="pokedex-filter">

        </div>
        <div class="pokedex-select">

        </div>
    </div>
</template>

<style lang="scss" scoped>
.pokedex-buttons {
    background-color: grey;
    width: 18%;
    border-radius: 40px 0 40px 0;
    margin-bottom: 20px;
}

.pokedex-filter {
    background-color: grey;
    width: 50%;
    border-radius: 0px 0px 40px 40px;
    margin-bottom: 20px;

}

.pokedex-select {
    background-color: grey;
    width: 18%;
    border-radius: 0px 40px 0px 40px;
    margin-bottom: 20px;

}
</style>