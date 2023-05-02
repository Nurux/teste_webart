<template>
<container>
    <header>
        <NavMenu @send="ola"></NavMenu>
        <img src="../assets/img/logo.jpg" alt="logo_wap.store">
        <InputSearch></InputSearch>
        <InputSearchDK></InputSearchDK>
        <div class="cadastro">
            <h3>Olá, bem vindo(a)!</h3>
            <p><a href="">Entre</a> ou <a href="">cadastre-se</a></p>
        </div>
        <div class="carrinho">
            <h3><strong>Meu Carrinho</strong></h3>
        </div>
        <NavBarDk @mn="ola"></NavBarDk>
    </header>

    <MenuLateral></MenuLateral>

    <main>
        <article>
            <Destaque></Destaque>
        </article>
        <aside>
            <ButtonFiltrar @filter="ola"></ButtonFiltrar>
            <Ordenacao></Ordenacao>
        </aside>
        <section id="port_products">
            <SpaceLeftVue></SpaceLeftVue>
            <section class="campo_produtos">
                <GridProdutos></GridProdutos>
                <Pagination></Pagination>
            </section>
        </section>
        
    </main>

    <footer>
        <p>2022 - Todos os direiros reservados | TESTE PARA DESENVOLVEDOR ASSISTENTE FRONTEND | CNPJ: 00.000.000/0000-00 BIRIGUI - SP</p>
        <img src="../assets/img/logo.jpg" alt="logo_wap.store">
    </footer>
</container>
</template>

<script>
import Pagination from '../components/mobile/Pagination.vue'
import GridProdutos from '../components/mobile/GridProdutos.vue';
import ButtonFiltrar from '../components/mobile/ButtonFiltrar.vue';
import InputSearch from '../components/mobile/InputMobile.vue';
import NavMenu from '../components/mobile/ButtonNavMobile.vue';
import MenuLateral from '../components/mobile/MenuLateralMobile.vue';
import Destaque from '../components/mobile/DestaqueMobile.vue';

import NavBarDk from '../components/desktop/NavBarDk.vue';
import InputSearchDK from '../components/desktop/InputSearchDK.vue';
import Ordenacao from '../components/desktop/Ordenacao.vue';
import SpaceLeftVue from '../components/desktop/SpaceLeft.vue';

export default{
    components: {
        NavMenu,
        InputSearch,
        MenuLateral,
        Destaque,
        ButtonFiltrar,
        GridProdutos,
        Pagination,
        NavBarDk,
        InputSearchDK,
        Ordenacao,
        SpaceLeftVue
       
    },
    methods: {
        ola
    }
}

function ola(){
    let menu_lateral = document.querySelector('.menu_lateral')
    let header = document.querySelector('header')

    menu_lateral.classList.toggle('active')
    header.classList.toggle('none')
}

</script>

<style scoped>
    *{
        padding: 0;
        margin: 0;
        font-family: Arial, Helvetica, sans-serif;
    }

    body{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    header{
        display: flex;
        flex-wrap: wrap;
        flex-direction: row;
        align-items: center;
        top: 0;
        position: sticky;
        border-bottom: 1px solid black;
        background-color: white;
    }

    header img{
       margin: auto;
       margin-left: -0.2rem;
    }

    header.none{
        border: none;
    }
    
    header .cadastro h3{
        font-size: 1rem;
        color: #ff4f01;
    }

    header .cadastro p{
        font-size: 0.8rem;
        text-align: left;
    }

    header .cadastro a {
        color: black;
    }

    header .carrinho h3 {
        color: #ff4f01;
        font-size: 1rem;
    }

    header .cadastro{
        display: none;
    }

    header .carrinho{
        cursor: pointer;
        display: none;
    }

    header .carrinho:hover{
        background-color: #9e9e9e50;
    }


    aside{
        display: flex;
        justify-content: center;
    }

    .campo_produtos{
        margin-top: 0.5rem;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }


    footer{
        display: flex;
        flex-direction: column;
        justify-content: center;
        justify-items: center;

        margin-top: 2rem;
    }
    footer p{
        color: #9E9E9E;
        font-size: 0.7rem;
        text-align: center;
        margin-bottom: 0.5rem;
    }

    footer img{
        width: 35%;
        margin: auto;
    }

    @media screen and (min-width: 590px){
        footer{
            width: 50vw;
            margin: auto;
            margin-top: 2rem;
        }
    }

    @media screen and (min-width: 900px) {
        header{
            z-index: 2;
            display: flex;
            align-items: center;
            justify-content: space-around;
            padding-top: 1rem;
            gap: 1rem;
            position: static;
        }

        header img {
            margin: 0;
        }
        header .cadastro{
            display: block;
        }

        header .carrinho{
            display: block;
        }

        aside{
            justify-content: flex-end;
        }

        #port_products {
            display: grid;
            grid-template-columns: 20% 80%;
            justify-items: center;
        }

        footer img{
            width: 10rem;
        }
    }
</style>
