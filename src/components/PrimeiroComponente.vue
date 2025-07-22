<template>
    <div>
        <h1>Primeiro Componente</h1>
    </div>
</template>

<!-- scoped = estilo aplicado apenas a esse componente -->
<style scoped>
    div{
        background-color: #0099ff;
        padding: 20px;
        margin: 30px;
        border-radius: 5px;
        text-align: center;
    }
    div:hover {
        background-color: #0033ff;
    }
    h1{
        color: white;
        margin-bottom: 10px;
    }
</style>