<template>
    <div class="pesquisa">
        <input type="text" placeholder="Procure por produtos, marcas ou nomes...">
        <button type="button"><img src="../../assets/img/icons/buscar.jpg" alt="icon_busca"></button>
    </div>
</template>

<script>
export default {
    name: 'InputSearch'
}
</script>

<style scoped>
*{
    margin: 0;
    padding: 0;
}
.pesquisa {
    display: flex;
    background-color: #F4F4F4;
}

.pesquisa input{
    font-size: 1rem;
    padding:0 1rem ;
    border: 1px solid #9E9E9E;
    border-radius: 0.5rem 0  0 0.5rem;
    height: 2.5rem;
    outline: none;
    width: 20rem;
}

.pesquisa button{
    border: none;
}

.pesquisa img{
    width: 3rem;
    height: 2.7rem;
}

.pesquisa {
    display: none;
}

@media screen and (min-width: 900px){
    .pesquisa{
        display: flex;
    }
}
</style>