<script>
export default {
    name: 'SelectForm',
    data: () => ({
        types: [
            "Bug",
            "Dark",
            "Dragon",
            "Electric",
            "Fairy",
            "Fighting",
            "Fire",
            "Flying",
            "Ghost",
            "Grass",
            "Ground",
            "Ice",
            "Normal",
            "Poison",
            "Psychic",
            "Rock",
            "Steel",
            "Water"
        ]
    })
};
</script>

<template>
    <select class="form-select">
        <option selected>All</option>
        <option v-for="type in types">{{ type }}</option>
    </select>
</template>

<style lang="scss" scoped>
select {
    width: 200px;
    border-radius: 0px 30px 0px 30px;
    text-align: center;
    font-size: 18px;
}
</style>