<template>
    <section class="destaque_produtos">
        <div class="select_produtos">
            <span><</span>
            <p id="home">Home |</p>
            <p>Eletrodomésticos</p>
         </div>

        <div class="info_produtos">
            <img src="../../assets/img/destaque-topo.png" alt="logo_eletrodomesticos">
            <div class="text">
                <h2>Eletrodomésticos</h2>
                <p>
                    Você consegue imaginar sua rotina sem os eletrodomésticos? Difícil, né? Eles são equipamentos essenciais para realizar as tarefas 
                    domésticas com praticidade e eficiência, além de oferecer conforto para o seu lar. Aqui na Dufrio você encontra diversas opções de 
                    eletrodomésticos para a cozinha, a lavanderia e outros ambientes da casa. <strong>Confira as nossas dicas de compra de eletrodomésticos na Dufrio!</strong>
                </p>
            </div>
        </div>

        <LeiaMais @leiamais="active"></LeiaMais>
    </section>
</template>

<script>
import LeiaMais from './LeiaMais.vue';

export default {
    components:{
        LeiaMais
    },
    methods: {
        active(){
            let leia = document.querySelector('.produtos_leia_mais')

            leia.classList.toggle('active')
        }
    }
}
</script>

<style scoped>
*{
    margin: 0;
    padding: 0;
}
.destaque_produtos{
    background-color: #edf5f8;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}
.select_produtos{
    width: 100vw;
    background-color: white;
    padding: 0.5rem 0;
    font-size: 0.7rem;
    color: #9E9E9E;
    display: flex;
    align-items: center;
}

.select_produtos #home{
    display: none;
}


.info_produtos{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;  
    background-color: #edf5f8;
}
.info_produtos h2{
    color: #ff4f01;
    text-align: center;
    margin-top: 1rem;
}

.info_produtos p{
    text-align: justify;
    margin: 0.5rem;
    font-size: 0.8rem;
    line-height: 1.2rem;
}

.info_produtos img{
    width: 100%;
}

.info_produtos button{
    border-radius: 0.2rem;
    margin: 1rem;
    text-align: center;
    width: 90%;
    height: 2rem;
    color: white;
    background-color: #ff4f01;
    border: none;
}
   
.produtos_leia_mais.active{
    display: block;
    border-top: 1px solid #9E9E9E;
    margin: 0.5rem;
    font-size: 0.8rem;
}

@media screen and (min-width: 900px) {
.destaque_produtos{
    border-bottom: 0.1rem solid rgb(0, 174, 255);
}
.select_produtos{
    width: 100vw;
    background-color: white;
    padding: 0.5rem 0;
    font-size: 0.7rem;
    color: #9E9E9E;
    display: flex;
    align-items: center;
}

.select_produtos #home{
    display: block;
}

.select_produtos p {
    margin: 0 0.2rem;
}

.select_produtos p:last-child{
    color: #ff4f01;
    font-size: 0.8rem;
    font-weight: bold;
}

.select_produtos span{
    display: none;
}


.info_produtos{
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;  
    background-color: #edf5f8;
}

.info_produtos .text{
    display: flex;
    flex-direction: column;
    text-align: left;
    margin:  0 0.7rem;
}

.info_produtos h2 {
    color: #ff4f01;
    text-align: left;
    margin-left: 0.5rem;
    margin-top: 1rem;
}

.info_produtos p{
    text-align: justify;
    font-size: 0.8rem;
    line-height: 1.2rem;
}

.info_produtos img{
    width: 100%;
}

.info_produtos a {
    margin-top: 1rem;
    color: #ff4f01;
}
   
.produtos_leia_mais.active{
    display: block;
    border-top: 1px solid #9E9E9E;
    margin: 0.5rem;
    font-size: 0.8rem;
}
}

</style>
