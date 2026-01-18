<script setup>
    import { ref } from 'vue';
    const cont = ref (0);

    function adicionar (){
        cont.value = cont.value+1
    }
    function diminuir (){
        if (cont.value > 0){
            cont.value = cont.value-1
        } else {
            return (
                alert("Não há como mais diminuir!")
            )
        }
    }
    function resetar (){
        cont.value = 0
    }
</script>
<template>
    <div>
        <h1>{{ cont }}</h1>
        <button @click="diminuir">-</button>
        <button @click="adicionar">+</button>
        <br>
        <button @click="resetar">Resetar</button>

    </div>
</template>