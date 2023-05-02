<template>
    <nav class="menu">
       <ul>
        <div>
            <li v-on:click="send">
            <a>
                <span class="material-symbols-outlined">menu</span>
                <p>Ver toda a loja</p>
                <span class="material-symbols-outlined">expand_more</span>
            </a>
            </li>
            <li><a href=""><img src="../../assets/img/icons/icon-ar.jpg" alt="icon_ar"><p>Ar condicionado</p></a></li>
            <li><a href=""><img src="../../assets/img/icons/icon-eletro.jpg" alt="icon_eletro1"><p>Eletrodoméstico</p></a></li>
            <li><a href=""><img src="../../assets/img/icons/icon-eletro2.jpg" alt="icon_eletro2"><p>Eletroportáteis</p></a></li>
            <li><a href=""><img src="../../assets/img/icons/industria.jpg" alt="icon_industry"><p>Comércio e Indústria</p></a></li>
            <li><a href=""><img src="../../assets/img/icons/icon-pecas.jpg" alt="icon_peca"><p>Peças</p></a></li>
            <li><a href=""><img src="../../assets/img/icons/icon-ferramentas.jpg" alt="icon_ferramenta"><p>Máquinas e Ferramentas</p></a></li>
            <li><a href=""><img src="../../assets/img/icons/icon-natal.jpg" alt="icon_natal"><p>Natal</p></a></li>
        </div>
       </ul>
    </nav>
</template>

<script>
export default {
    emits: ['mn'],
    methods: {
        send(){this.$emit('mn', true)}
    }
}

</script>

<style scoped>
    *{
        margin: 0;
        padding: 0;
    }

    nav {
        display: none;
    }

    ul{
        display: flex;
        justify-content: space-around;
        align-items: center;
        list-style: none;
        height: 3rem;
        background-color: #ff4f01;
        width: 100vw
    }

    div{
        display: flex;
        width: 80vw;
    }

    li{
        cursor: pointer;
        display: flex;
        justify-content: center;
        background: #ff4f01;
        max-height: 3rem;
    }

    ul li:not(:last-child){
        border-right: 2px solid rgb(18, 18, 136);
    }

    

    a{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-decoration: none;
        padding: 1rem;
        color: white;
    }

    a img{
        width: 2rem;
        height: 1.5rem;
    }

    a p {
        font-size: 0.7rem;
    }

    a span:first-child{
        display: none;
    }

    a span{
        color: rgb(18, 18, 136);
    }


    ul li:first-child{
        display: flex;
        align-items: center;
        justify-items: center;
        width: 10rem;
    }

    ul li:first-child a{
        display: flex;
        flex-direction: row;
        width: 10rem;
        background-color: rgb(255, 255, 255);
        color: #ff4f01;
    }

    li:hover{
        background-color: rgba(0, 0, 0, 0.084);
    }


    @media  screen and (min-width: 900px) {
        nav {
            display: block;
        }

        ul{
            height: 4rem;
        }

        li{
            width: 100%;
        }
    }

    @media screen and (min-width: 1390px){
        ul{
            height: 3rem;
        }

        a span:first-child{
            display: block;
            margin-right: 0.2rem;
        }
    }
</style>