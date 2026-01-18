<script setup>
    const frutas = [
        "Banana",
        "Maçã",
        "Mamão",
        "Uva", 
        "Morango",
    ]
</script>
<template>
    <div>
        <h3>Lista de compras</h3>
        <ul>
            <li v-for="fruta in frutas" :key="fruta">
                {{ fruta }}
            </li>
        </ul>
    </div>
</template>