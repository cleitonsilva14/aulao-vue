<template>
    <div class="componente">
        <h1>Componente com Renderização de Lista</h1>
        <p>Nome: {{ nome }}</p>
        <p v-show="passaros.length === 0">Não tem pássaros</p>
        <ul>
            <li v-for="passaro in passaros">
                Nome: {{ passaro.nome }} | Idade: {{ passaro.idade }}
            </li>
        </ul>
    
    </div>
</template>

<script setup>
    import { defineProps } from 'vue';
    defineProps({
        nome: String,
        passaros: Array
    })



</script>


<style scoped>
    ul {
        margin: 0px;
        padding: 0px;
    }

    li {
        list-style: none;
        text-align: center;
        font-size: large;
    }

</style>