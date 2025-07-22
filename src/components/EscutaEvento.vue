<!-- 1h15 -->
<template>
   <div class="componente">
      <h1>Componente que Escuta Evento</h1>
      <p>Total: R$ {{ total.toFixed(2) }}</p>
      <div class="lista">
         <EmiteEvento item="Item 1" :preco="2.50" @adicionado="atualizarTotal" />

         <EmiteEvento item="Item 2" :preco="10.50" @adicionado="atualizarTotal" />

         <EmiteEvento item="Item 3" :preco="3.50" @adicionado="atualizarTotal" />
      </div>
   </div>
</template>

<script setup>

import { ref } from 'vue';
import EmiteEvento from './EmiteEvento.vue';

const total = ref(0)

function atualizarTotal(p) {

   const valor = total.value + p

   total.value = +valor.toFixed(2)
}


</script>

<style scoped>
.lista {
   display: flex;
   justify-content: space-between;
}
</style>
