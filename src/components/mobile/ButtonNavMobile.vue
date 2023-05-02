<template>
    <nav>
        <button type="button" id="menu" v-on:click="send">
                <div></div>
                <div></div>
                <div></div>
        </button>
    </nav>
</template>

<script>
    export default{
        name: 'NavButton',
        emits: ['send'],
        methods: {
            send(){this.$emit('send', true)}
        }
    }

    
</script>

<style scoped>

button{
    width: 2.5rem;
    height: 2rem;
    margin: 1rem;
    border: none;
    background-color: white;
}

button div {
    background-color: #1E90FF;
    height: 0.2rem;
    margin: 0.3rem 0 0.4rem 0;
}
        
button:hover{
    cursor: pointer;
    background-color: rgba(224, 224, 224, 0.97);
}

@media  screen and (min-width: 900px) {
    nav{
        display: none;
    }
}
</style>