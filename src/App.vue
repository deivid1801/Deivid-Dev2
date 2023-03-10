<script setup>
  
  import { ref, onMounted } from 'vue'

const contador = ref(0)

function incrementarContador() {
  contador.value++
}
function decrementarContador() {
  contador.value--
}

onMounted(() => {
  console.log(`O valor inicial do contador é ${contador.value}.`)
})  
const rawHtml = '<span style="color: red">Este é um texto em vermelho</span>'
function reiniciarContador(){
  contador.value = 0
}
</script>

<template>
  <button @click="incrementarContador">Incrementar</button>
  <button @click="reiniciarContador">Reiniciar</button>
  <button @click="decrementarContador">Decrementar</button>
  <p>Valor do contador é: {{ contador }}</p>
<p>Usando interpolação de textos: {{rawHtml}}</p>
    <p>Usando v-html: <span v-html="rawHtml"></span></p>
</template>

<style scoped>
button {
  font-weight: bold;
}
</style>
