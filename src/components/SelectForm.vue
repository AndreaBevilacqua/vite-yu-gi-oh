<script>
export default {
    name: 'SelectForm',
    props: {
        default: String,
        defaultValue: String,
        options: Array
    }
};
</script>

<template>
    <select class="form-select">
        <option :value="defaultValue || ''">{{default }}</option>
        <option v-for="(option, i) in options" :key="i">{{ option }}</option>
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