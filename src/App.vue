<script setup lang="ts">
import { ref } from 'vue';
import Click from './components/Click.vue';
import Contador from './components/Contador.vue';
import Input from './components/Input.vue';
import LoginLogout from './components/LoginLogout.vue';
import Lista from './components/Lista.vue';
import ToDo from './components/ToDo.vue';
import ContCaracteres from './components/ContCaracteres.vue';
import Filtro from './components/Filtro.vue';
import ProjectCard from './components/ProjectCard.vue';
import UserCard from './components/Props/UserCard.vue';
 const projects = [
  {id:1, name: ' Alerta - Bem vindo', key: 'click' },
  {id:2, name: 'Contador', key: 'contador' },
  {id:3, name: 'Login e Logout', key: 'loginLogout' },
  {id:4, name: 'Input espelhado', key: 'input' },
  {id:5, name: 'Lista simples', key: 'lista' },
  {id:6, name: 'To-do List', key: 'todo' },
  {id:7, name: 'Contador de Caracteres', key: 'contadorCaracter' },
  {id:8, name: 'Filtro por status e nome', key: 'filter' },
  {id:9, name: 'Card de Users', key: 'userCard' }
 ]
const isSelected = ref<string | null>(null);

function openProject (key:string){
  isSelected.value = key
}

</script>

<template>
  <main>
    <h1>Vue Playground</h1>
    <p>Este site é um playground para treinar Vue.js.
    Aqui testo componentes, lógica, estados e ideias enquanto aprendo e evoluo no framework.</p>
    <br>
    <div class="">
    <ProjectCard
      v-for="project in projects"
      :key="project.id"
      :project="project"
      @ver-projeto="openProject"
    />
    </div>
    <div>

      <br>
      <hr>
      <h2>Projeto</h2>
    <Contador v-if="isSelected === 'contador'" />
    <Input v-if="isSelected === 'input'" />
    </div>
    <LoginLogout v-if="isSelected === 'loginLogout'" />
    <Lista v-if="isSelected === 'lista'"/>
    <Click v-if="isSelected === 'click'"/>
    <ToDo v-if="isSelected === 'todo'" />
    <ContCaracteres v-if="isSelected === 'contadorCaracter'" />
    <Filtro v-if="isSelected === 'filter'" />
    <UserCard v-if="isSelected === 'userCard'" />
  </main>
</template>

<style scoped>

</style>
