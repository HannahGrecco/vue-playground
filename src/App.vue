<script setup lang="ts">
import Click from './components/Click.vue';
import Contador from './components/Contador.vue';
import Input from './components/Input.vue';
import LoginLogout from './components/LoginLogout.vue';
import Lista from './components/Lista.vue';
import ToDo from './components/ToDo.vue';
import ContCaracteres from './components/ContCaracteres.vue';
import Filtro from './components/Filtro.vue';
</script>

<template>
  <main>
    <div>
      <h1>Vue Playground</h1>
      <p>Isto é um simples playground em Vue</p>
      <p>Usado para treinar funções, diretivas, eventos e etc em Vue</p>
    </div>
    <hr>
    <div>
      <h2>Simples @click</h2>
      <Click />
      <hr>
      <h2>Contador</h2>
      <Contador />
      <hr>
      <h2>Login e Logout</h2>
      <LoginLogout />
      <hr>
      <h2>Input Espelho</h2>
      <Input />
      <hr>
      <h2>Lista Simples</h2>
      <Lista />
      <hr>
    </div>
    <div>
      <h1>Nível 2</h1>
      <hr>
      <div>
        <h2>To-Do List</h2>
        <ToDo />
      </div>
      <hr>
      <div>
        <h2>Contador de caracteres</h2>
        <ContCaracteres />
      </div>
      <hr>
      <div>
        <h2>Filtro por status e nome</h2>
        <Filtro />
      </div>
    </div>
  </main>
</template>

<style scoped>

</style>
