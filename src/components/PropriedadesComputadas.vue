<!-- 1h31m -->


<template>
    <div class="componente">
        <h1>Propriedades Computadas</h1>
        <p>Idade: {{ idade }}</p>

        <label for="">Ano de Nascimento</label>
        <p><input type="number" v-model="anoNascimento" min="1900"></p>
        <label for="">Ano Atual:</label>
        <p><input type="number" v-model="anoAtual" min="2000"></p>
    </div>
</template>

<script setup>
    import { ref , computed } from 'vue';

    const currentYear = new Date().getFullYear();

    const anoNascimento = ref(1900)
    const anoAtual = ref(currentYear)
    
    const idade = computed(() => {
        return anoAtual.value - anoNascimento.value
    }) 


</script>

<style scoped>

    label{
        margin: 10px;
    }

</style>