<script>
export default {
    name: 'SelectForm',
    data: () => ({ selectedOption: '' }),
    props: {
        default: String,
        defaultValue: String,
        options: Array
    },
    emits: ['option-change']
};
</script>

<template>
    <select class="form-select" v-model="selectedOption" @change="$emit('option-change', selectedOption)">
        <option :value="defaultValue || ''">{{default }}</option>
        <option v-for="(option, i) in options" :key="option.id" :value="option.value">{{ option.label }}</option>
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