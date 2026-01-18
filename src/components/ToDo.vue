<script setup>
    import { ref } from 'vue';

    const inputText = ref("");
    const tasks = ref([""]);

    function addTask(){
        if (inputText.value.trim() === '')
        return
            tasks.value.push(inputText.value)
            inputText.value = ''
    }
    function deleteTask(index){
        tasks.value.splice(index,1)
    }

</script>
<template>
    <div>
        <label>
            <input v-model="inputText" placeholder="Digite sua tarefa" type="text">
            <button @click="addTask">Adicionar Tarefa</button>
            
            <ul>
                <li v-for="(task, index) in tasks" :key="index">
                    {{ task }}
                    <button @click="deleteTask">Deletar tarefa</button>
                </li>
            </ul>
        </label>
    </div>
</template>