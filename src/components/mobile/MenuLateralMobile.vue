<template>
    <nav>
        <div class="menu_lateral">
            <ul>
                <li><a href="">Ar condicionado</a> <span class="material-symbols-outlined">chevron_right</span></li>
                <li><a href="">Ventilação</a> <span class="material-symbols-outlined">chevron_right</span></li>
                <li><a href="">Eletrodoméstico</a> <span class="material-symbols-outlined">chevron_right</span></li>
                <li><a href="">Eletroportáteis</a> <span class="material-symbols-outlined">chevron_right</span></li>
                <li><a href="">Casa Inteligente</a> <span class="material-symbols-outlined">chevron_right</span></li>
                <li><a href="">Comércio e Indústria</a> <span class="material-symbols-outlined">chevron_right</span></li>
                <li><a href="">Máquinas e Ferramentas</a> <span class="material-symbols-outlined">chevron_right</span></li>
                <li><a href="">Materiais de Instalação</a> <span class="material-symbols-outlined">chevron_right</span></li>
                <li><a href="">Fluído Gás Refrigerante</a> <span class="material-symbols-outlined">chevron_right</span></li>
                <li><a href="">Peças</a> <span class="material-symbols-outlined">chevron_right</span></li>
            </ul>
        </div>
    </nav>
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

.menu_lateral{
    display: none;
    border-top: 1px solid rgb(191, 190, 190);
}

.menu_lateral li{
    color: #9E9E9E;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-direction: row;
    padding: 0.9rem;
}
            
.menu_lateral a{
    color: #9E9E9E;
    text-decoration: none;
}

.menu_lateral li:hover{
    cursor: pointer;
    background-color: rgb(238, 238, 238);
}

.menu_lateral.active{
    display: block;
    position: fixed;
    background-color: white;
}

@media screen and (min-width: 900px){
    .menu_lateral.active{
       border: 1px solid #9E9E9E;
       position: absolute;
       left: 9rem;
       max-width: 10.5rem;
    }

    .menu_lateral a{
        font-size: 0.6rem;
    }
}
</style>