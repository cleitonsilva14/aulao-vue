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
import PropriedadesAssistidas from './components/PropriedadesAssistidas.vue';
import RenderizacaoCondicional from './components/RenderizacaoCondicional.vue';
import RenderizacaoListas from './components/RenderizacaoListas.vue';
import Slots from './components/Slots.vue';

// comunicação PAI -> Filho (utilizando props)
const borracha = "Borracha Azul"
const precoBorracha = 2.50

const birds = [
  { nome: "Lilica", idade: 1 },
  { nome: "Pipoca", idade: 1 },
  { nome: "Faisca", idade: 1 }
]

</script>

<!-- HTML -->
<template>
  <header>Vue</header>

  <Slots>
    <template v-slot:icone>
      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
        stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
        class="icon icon-tabler icons-tabler-outline icon-tabler-home">
        <path stroke="none" d="M0 0h24v24H0z" fill="none" />
        <path d="M5 12l-2 0l9 -9l9 9l-2 0" />
        <path d="M5 12v7a2 2 0 0 0 2 2h10a2 2 0 0 0 2 -2v-7" />
        <path d="M9 21v-6a2 2 0 0 1 2 -2h2a2 2 0 0 1 2 2v6" />
      </svg>
      
    </template>
    <template v-slot:texto>
      Home
    </template>

  </Slots>

  <RenderizacaoListas nome="Maria" :passaros="birds" />

  <RenderizacaoCondicional nome="Maria" :quantidade="0" />

  <PropriedadesAssistidas />

  <PropriedadesAssistidas />

  <PropriedadesComputadas />

  <EscutaEvento />

  <!-- comunicação PAI -> Filho (utilizando props) -->
  <ComProps :item="borracha" :preco="precoBorracha" />

  <ComProps item="Smartwatch" :preco="259.99" />
  <ComProps item="Impressora" :preco="950.90" />
  <ComProps item="TV" :preco="2559.99" />
  <DataBinding />
  <ComDadosReativosPrimitivosNaoPrimitivos />
  <ComDadosReativosPrimitivos />
  <ComDados />
  <PrimeiroComponente />
</template>

<!-- CSS -->
<style scoped></style>
