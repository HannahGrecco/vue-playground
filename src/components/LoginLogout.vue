<script setup>
    import { ref } from 'vue';
    const isLogged = ref(false)
    function auth () {
        isLogged.value = !isLogged.value
    }
</script>
<template>
    <div>
        
        <button @click="auth">
            {{ isLogged ? 'Logout' : 'Login' }}
        </button>
        <p v-if="isLogged">Você está logado</p>
        <p v-else>Você está deslogado</p>
    </div>
</template>