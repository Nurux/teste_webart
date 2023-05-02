<template>
<div class="grid_produtos">
    <Produtos></Produtos>
</div>
</template>

<script>
import Produtos from './Produtos.vue';

export default {
    components: {
        Produtos
    }
}
</script>

<style scoped>
.grid_produtos{
    margin: 1rem 0;
    display: grid;
    background-color: rgb(238, 238, 238);
    grid-template-columns: 50% 50%;
    max-width: 100vw;
}

@media screen and (min-width: 900px){
    .grid_produtos{
        grid-template-columns: 33% 33% 33%;
        gap: 0.3rem;
    }
}
</style>