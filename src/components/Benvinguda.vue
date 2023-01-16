<template>
    <div class="inici">
        <h1>Gestió Empresarial VUE</h1>
        <p>Benvingut/da al nostre tutorial per a nous usuaris</p>
        <p>A continuació et mostrem un petit tutorial. Pots navegar pels botons per accedir als diferents consells.</p>

        <button @click="$emit('cambia',1)">Iniciar</button>
    </div>
</template>

<script>
    export default {
        name: 'Benvinguda',
        emits: ['cambia']
    }
</script>