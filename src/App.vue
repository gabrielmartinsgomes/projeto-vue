<script setup>
import { ref, onMounted } from 'vue'

const contador = ref(0)

function incrementarContador() {
  contador.value++
}
function decrementarContador() {
  contador.value--
}
function zerarContador() {
  contador.value=0
}

onMounted(() => {
  console.log(`O valor inicial do contador é ${contador.value}.`)
})
</script>


<template>
     <button @click="incrementarContador">+</button>
  <button @click="decrementarContador">-</button>
  <button @click="zerarContador">Zerar</button>
  <p>Valor do contador é: {{ contador }}</p>
</template>

<style scoped>
button {
  font-weight: bold;
  color: white;
  background-color: black;
  margin: 1px;
  
}
</style>