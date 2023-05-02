<template>
    <button type="button" v-on:click="filter">Filtrar</button>
</template>

<script>
export default {
    emits: ['filter'],
    methods: {
        filter(){this.$emit('filter', true)}
    }
}
</script>

<style scoped>
    button{
        cursor: pointer;
        border-radius: 0.2rem;
        text-align: center;
        width: 90%;
        background-color: #ff4f01;
        border: none;
        color: white;
        height: 2.5rem;
    }

    @media  screen and (min-width: 900px) {
        button{
            display: none;
        }
    }
</style>