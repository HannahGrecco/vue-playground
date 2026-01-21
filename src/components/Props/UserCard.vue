<script setup>
    const props = defineProps({
        name: String,
        email: String,
        isActive: Boolean
    })
</script>

<template>

    <p>{{ name }}</p>
    <p>{{ email }}</p>
    <span>{{ isActive ? 'Ativo' : 'Inativo'  }}</span>
</template>