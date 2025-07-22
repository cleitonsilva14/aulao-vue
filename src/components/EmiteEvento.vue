<!-- 1h15 -->
<template>
   <div class="componente">
       <h1>Componente que Emite Evento</h1>
       <p>{{ item }} {{ preco.toFixed(2) }}</p>
       <button @click="adicionar"> + Cart</button>
   </div>
</template>

<script setup>

    import { defineProps, defineEmits } from 'vue'

    const props  = defineProps({
        item: String, 
        preco: Number
    })


    const emit = defineEmits(["adicionado"])

    function adicionar(){
        emit("adicionado", props.preco)
    }




</script>