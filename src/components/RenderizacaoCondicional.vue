<template>
    <div class="componente">
        <h1>Componente com Renderização Condicional</h1>
        <p>Nome: {{ nome }}</p>
    
        <p v-if="quantidade === 0">Não tem Pássaros</p>
        <p v-else-if="quantidade === 1">Tem um Pássaro</p>
        <p v-else>Tem muitos Pássaros</p>
    
    </div>
</template>

<script setup>
    import { defineProps } from 'vue';
    defineProps({
        nome: String,
        quantidade: Number
    })



</script>