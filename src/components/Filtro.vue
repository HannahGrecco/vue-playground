<script setup>
import { ref, computed } from 'vue'

const search = ref('')
const is_active = ref(false)

const lists = ref([
  { id: 1, name: 'name1', active: false },
  { id: 2, name: 'name2', active: true },
  { id: 3, name: 'name3', active: false }
])

const filteredLists = computed(() => {
  return lists.value
    .filter(item =>
      item.name.toLowerCase().includes(search.value.toLowerCase())
    )
    .filter(item =>
      !is_active.value || item.active
    )
})
</script>

<template>
  <div>
    <input v-model="search" placeholder="Buscar nome" />

    <label>
      <input type="checkbox" v-model="is_active" />
      Mostrar apenas ativos
    </label>

    <ul>
      <li v-for="list in filteredLists" :key="list.id">
        {{ list.name }}
      </li>
    </ul>
  </div>
</template>
