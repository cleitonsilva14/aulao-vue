<!-- 52:51 -->
<template>
    <div class="componente">
        <h1>Componente com Data Binding</h1>
        <p>{{ valor3 }}</p>
        <input type="text" v-bind:value="valor">
        
        <!-- v-bind:value="valor2" = :value="valor2" -->
         <!-- v-on:input="" = @:input -->
        <input type="text" 
        :value="valor2"
        @:input="(evento) => valor2 = evento.target.value">
    

        <!-- já faz com evento -->
        <input type="text"
        v-model="valor3"
        >

    </div>
</template>


<script setup>

import {ref } from "vue"

// OneWay DataBinding
// Javascript => HTML
const valor = ref("Fixo  !")

// To Way DataBinding (não mais otimizado)
// Javascript <=> HTML
const valor2 = ref("vuejs valor2")

const valor3 = ref("valor3")


</script>