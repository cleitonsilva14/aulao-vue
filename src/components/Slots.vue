<template>

    <div class="componente">
        <h1>Componente Com Slots</h1>
        <button>
            <slot name="icone"/>
            <slot name="texto">
                Botão
            </slot>
        </button>
    </div>

</template>