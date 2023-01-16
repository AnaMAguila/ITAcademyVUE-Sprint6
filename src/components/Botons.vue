<template>
    <div>
        <button @click="$emit('accio',0)">Anterior</button>
        <button @click="$emit('accio',1)">Següent</button>
    </div>
</template>

<script>
    export default {
        name: 'Botons',
        emits: ['accio']
    }
</script>