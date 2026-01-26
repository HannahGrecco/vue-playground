<script setup>
const props = defineProps({
  project: Object
})

const emit = defineEmits(['ver-projeto'])

function handleClick() {
  emit('ver-projeto', props.project.key)
}
</script>

<template>
  <div class="container">
    <h3>{{ project.name }}</h3>
    <button @click="handleClick">
      Ver projeto
    </button>
  </div>
</template>
