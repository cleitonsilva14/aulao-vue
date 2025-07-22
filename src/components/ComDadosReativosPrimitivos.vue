<template>
    <div class="componente">
        <h1>Componente com dados Reativos Primitivos</h1> <!-- MasterClass VueJS 2024 Minutos 45:18 -->
        <p>Nome: {{ nome }} | Idade: {{ idade }}</p>
        <button v-on:click="fazNiver()">Niver</button>
        <button @click="mudarNome()">Mudar Nome</button>
    </div>
</template>

<script setup>

    import {ref} from "vue"

    const nome = ref("Vue")
    const idade = ref(10)
    
    function fazNiver(){
        idade.value++
    }

    function mudarNome(){
        nome.value = "Maria Cecilia"
    }

</script>

<style scoped>
</style>
