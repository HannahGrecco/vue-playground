<script setup>
    import { ref } from 'vue';
    const name = ref("");

</script>
<template>
    <div>
        <label for="">
         <input v-model="name" placeholder="Digite seu nome" 
         type="text">
         <p>{{ name }}</p>
        </label>
    </div>
    
    
</template>