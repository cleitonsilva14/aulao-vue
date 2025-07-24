<!-- Javascript -->
<script setup>
import PrimeiroComponente from './components/PrimeiroComponente.vue';
import ComDados from './components/ComDados.vue'
import ComDadosReativosPrimitivos from './components/ComDadosReativosPrimitivos.vue';
import ComDadosReativosPrimitivosNaoPrimitivos from './components/ComDadosReativosPrimitivosNaoPrimitivos.vue';
import DataBinding from './components/DataBinding.vue';
import ComProps from './components/ComProps.vue';
import EscutaEvento from './components/EscutaEvento.vue';
import PropriedadesComputadas from './components/PropriedadesComputadas.vue';

// comunicação PAI -> Filho (utilizando props)
const borracha = "Borracha Azul"
const precoBorracha = 2.50
</script>

<!-- HTML -->
<template>
  <header>Vue</header>

  <PropriedadesComputadas/>

  <EscutaEvento/>

   <!-- comunicação PAI -> Filho (utilizando props) -->
  <ComProps :item="borracha" :preco="precoBorracha"/>
  
  <ComProps item="Smartwatch" :preco="259.99"/>
  <ComProps item="Impressora" :preco="950.90"/>
  <ComProps item="TV" :preco="2559.99"/>
  <DataBinding/>
  <ComDadosReativosPrimitivosNaoPrimitivos/>
  <ComDadosReativosPrimitivos/>
  <ComDados/>
  <PrimeiroComponente/>
</template>

<!-- CSS -->
<style scoped>

</style>
