<template>
    <section>
        <div class="categorias">
            <h4>Categorias</h4>
            <a href="">Adega de Vinho</a>
            <a href="">Champanheira Elétrica</a>
            <a href="">Churrasqueira</a>
            <a href="">Coifa</a>
            <a href="">Cooktop</a>
            <a href="">Depurador de Ar</a>
            <a href="">Fogão a Gás</a>
            <a href="">Forno a Gás</a>
            <a href="">Forno Elétrico</a>
            <a href="">Frigobar</a>
            <a href="">Ver mais</a>
        </div>
        <div class="marcas">
            <h4>Marcas</h4>
        </div>
        <div class="precos">
            <h4>Preços</h4>
            <label><input type="checkbox">R$665,00 a 5573,00</label>
            <label><input type="checkbox">R$5573,01 a 10480,00</label>
            <label><input type="checkbox">R$10480,01 a 15388,00</label>
            <label><input type="checkbox">R$15388,01 a 20295,00</label>
            <label><input type="checkbox">R$20295,01 a 25203,00</label>
        </div>
    </section>    
</template>



<script>
export default {
    
}
</script>



<style scoped>
    section{
        display: none;
        flex-direction: column;
        align-items: center;
        color: #9E9E9E;
    }

    .marcas{
        margin: 1rem;
        margin-top: 2rem;
    }
    .marcas h4{
        text-align: left;
        margin: 0;
        padding: 0;
    }

    a{
        color: #9E9E9E;
    }

    div {
        width: 100%;
        display: flex;
        flex-direction: column;
        text-align: left;
    }

    h4{
        color: #ff4f01;
    }

    .categorias a:not(:last-child){
        text-decoration: none;
    }

    @media screen and (min-width: 900px){
        section{
            display: flex;
        }
    }
</style>