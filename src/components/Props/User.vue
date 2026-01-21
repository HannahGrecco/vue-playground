<script setup>
import UserCard from './UserCard.vue';
import { ref } from 'vue';

    const users = ref([
        { id: 1, name: 'Hannah', email: 'Hannah@gmail.com', isActive: false },
        { id: 2, name: 'João', email: 'Joao@gmail.com', isActive: true },
        { id: 3, name: 'Túlio', email: 'Tulio@gmail.com', isActive: true },
])
</script>
<template>
    <div>
        <h2>User Card</h2>
        <UserCard
            v-for="user in users"
            :key="user.id"
            :name="user.name"
            :email="user.email"
            :isActive="user.isActive"
        
        />
    </div>
</template>