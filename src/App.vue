<script setup> 

import {ref }from 'vue'

let contador = ref(0)

function contadorMais(){
    contador.value++
}
function contadorMenos(){
    if (contador.value > 0) {
      contador.value--
    }
}
function limpar(){
  contador.value = 0
}


</script>

<template>

  <button @click="contadorMais()">+</button>
  <button @click="contadorMenos()">-</button>
   <p> Valor do contador: {{ contador }}</p>
  <button @click="limpar()">Limpar</button>

</template>

<style scoped> 

button{
  background-color: rgb(104, 172, 250);
  color: white;
  font-weight: bold;
  border: 0;
  margin: 2px;
  padding: 20px;
}

</style>