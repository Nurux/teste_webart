<template>
    <div class="ordenation_inputs">
        <label for="itens">Itens por pagina:</label>
        <select name="itens">
            <option value="12">12</option>
            <option value="24">24</option>
            <option value="36">36</option>
        </select>
        <label for="order">Ordenar por:</label>
        <select name="order">
            <option value="popular">Popularidade</option>
            <option value="minipreco">Maior Preço</option>
            <option value="maxpreco">Menor Preço</option>
        </select>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
*{
    margin: 0;
    padding: 0;
}

.ordenation_inputs{
    display: none;
}



@media screen and (min-width: 900px){
    .ordenation_inputs{ 
        display: block;
        margin-top: 1rem;
    }   

    select{
        margin-right: 1rem;
        margin-left: 0.2rem;
        height: 2rem;
    }
}
</style>