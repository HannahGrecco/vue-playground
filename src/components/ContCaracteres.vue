<script setup>
    import { ref, computed } from 'vue';

    const text = ref("");
    
    const countText = computed(() => {
        return text.value.length
    })
</script>
<template>
    <div>
        <input v-model="text" placeholder="Digite aqui" type="text">
        <p>Caracteres: {{ countText }}</p>
    </div>
</template>