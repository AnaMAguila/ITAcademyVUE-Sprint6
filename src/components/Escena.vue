<template>
    <div>
        <!-- MUESTRA LOS DATOS DEL ARCHIVO JSON (Ahora js)  -->            
        <ul>
            <li v-for="(text, index) in arrayFrases" 
            :key="index"
            :class="{ active: index === currentSentence}"
            >
                {{ text.txt }}
            </li>
        </ul>
   
    </div>
</template>

<script>
    export default {
        name: 'Escena',
        props: ['arrayFrases','currentSentence'],
    }
</script>