<!-- 1h04min -->

<template>
    <div class="componente">
        <h1>Props</h1>
        <p>{{ item }} R${{ preco.toFixed(2) }}</p>
    </div>
</template>
<script setup>

import { defineProps } from 'vue';

// 
defineProps({
    item: String,
    preco: Number
})



</script>