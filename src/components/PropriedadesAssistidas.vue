<!-- 1h 39 -->
<template>

    <div class="componente">
        <h1>Propriedades Assistidas</h1>
        <p>Idade: {{ idade }}</p>
        <p>
            <label for="">Nascimento: </label>
            <input type="number" v-model="anoNasc" min="1900">
        </p>
        <p>
            <label for="">Ano Atual: </label>
            <input type="number" v-model="anoAt" min="2000">
        </p>
        
    </div>


</template>


<script setup>

// propriedade assistida - executa ação quando variável for alterada

import { ref } from 'vue'
// import { watch } from 'vue'

import { watchEffect } from 'vue'

const anoNasc = ref(1900)
const anoAt = ref(2000)
const idade = ref(0)

/*
watch(anoAt, (ano) => {
    idade.value = ano - anoNasc.value
})

watch(anoNasc, (ano) => {
    idade.value = anoAt.value - ano
})
*/

watchEffect(()=>{
    idade.value = anoAt.value - anoNasc.value
})

</script>