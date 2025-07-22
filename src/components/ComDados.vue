<template>
    <div>
        <h1>Componente Dados</h1>
        <p>Nome: {{nome}} - {{ codigo }}</p>
    </div>
</template>

<style scoped>
    div{
        text-align: center;
        border: 2px solid #1fd50b;
        background-color: #010810;
        border-radius: 15px;
        margin: 30px;
        padding: 10px;
    }
    p{
        font-size: 1.2rem;
    }
</style>

<!-- composition API melhor -->
<script setup>
    const nome = "tv"
    const codigo = 1000
</script>

<!-- <script>
// options API
/*export default {
    data:function(){
        return {
            nome: "TV",
            codigo: "#321"
        }
    }
}*/
//composition API 
/*export default {
    setup: function(){
        const nome = "Smartwatch"
        const codigo = 4000
        return {nome, codigo}
    }
}*/
</script> -->