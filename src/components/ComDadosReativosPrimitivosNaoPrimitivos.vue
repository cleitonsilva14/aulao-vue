<template>
    <div class="componente">
        <h1>Componente com dados Reativos Não Primitivos</h1> 
        <p>Nome: {{ user.nome }} | Idade: {{ user.idade }}</p>
        <button @click="fazNiver()">Aniversário++</button>
        <button @click="mudarNome()">Mudar Nome</button>
    </div>
</template>

<!-- Reactive (composition API) -->
<!-- <script setup>

    import { ref } from "vue"
    import { reactive } from "vue"

    const user = reactive({nome: "admin", idade: 10})

    function fazNiver(){
        user.idade++
    }

    function mudarNome(){
        user.nome = "ADMIN"
    }

</script> -->


<!-- Option API -->
<!-- Vue já sabe que são dados que vão se alterar -->
 <script>
 export default {
    data: function(){
        return {
            user: {
                nome: "administrador",
                idade: 10
            }
        }
    },
    methods:{
        fazNiver:function(){
            this.user.idade+=1
        },
        mudarNome:function(){
            this.user.nome = "ADMIN 2"
        }
    }
 }
</script>

<style scoped>
</style>
