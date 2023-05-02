<template>
<div class="pagination">
    <p>Produtos 1-12 de 284 encontrado(s)</p>
    <ul>
        <li class="arrow"><span class="material-symbols-outlined">keyboard_double_arrow_left</span><p>Primeira</p></li>
        <li class="arrow"><span class="material-symbols-outlined">chevron_left</span><p>Anterior</p></li>
        <li style="color: white; background-color: #ff4f01; border: none;">1</li>
        <li>2</li>
        <li>3</li>
        <li>4</li>
        <li>5</li>
        <li class="arrow"><p>Proxima</p><span class="material-symbols-outlined">chevron_right</span></li>
        <li class="arrow"><p>Última</p><span class="material-symbols-outlined">keyboard_double_arrow_right</span></li>
    </ul>
</div>
</template>

<script>
export default {
    
}
</script>


<style scoped>
*{
    padding: 0;
    margin: 0;
}
.pagination{
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 60vw;
    margin-top: 2rem;
}

p{
    font-size: 0.7rem;
}

ul{
    display: flex;
    justify-content: center;
    align-items: center;
    list-style: none;
    gap: 0.5rem;
    margin-top: 0.5rem;
}

li{
        cursor: pointer;
        display: flex;
        justify-content: center;
        align-items: center;
        width: 2rem;
        height: 1.6rem;
        border: 1px solid rgba(128, 128, 128, 0.338);
        border-radius: 0.2rem;
}


li:hover{
    background-color: #ff4f01;
    border: none;
    color: white;
}

ul li p{
    display: none;
}

ul li:first-child{
    display: none;
}

ul li:last-child{
    display: none;
}


@media screen and (min-width: 900px){
    .pagination{
        flex-direction: row;
        width: 80vw;
        justify-content: space-between;
    }

    li.arrow{
        width: 5rem;
    }

    ul li p{
        display: flex;
    }

    ul li:first-child{
        display: flex;
    }

    ul li:last-child{
        display: flex;
    }

    ul{
        margin-right: 1rem;
    }

    .pagination p {
        padding: 0;
        margin: 0;
    }

}

</style>