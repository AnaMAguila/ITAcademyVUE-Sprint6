<template>
    <div>
        <!-- Dejo las dos formas de leer el array: -->
        <!-- MUESTRA LOS DATOS DEL DATA HOME.VUE -->
        <ul>
            <li v-for="(text, index) in frases" 
            :key="index"
            :class="{ active: index === currentSentence}"
            >
                {{ text }}
            </li>
        </ul>

        <!-- MUESTRA LOS DATOS DEL ARCHIVO JSON  -->            
        <!-- <ul>
            <li v-for="text in obtenFrases" :key="text">
                {{ text }}
            </li>
        </ul> -->
   
    </div>
</template>

<script>
    // IMPORTA LOS DATOS DEL ARCHIVO JSON  
    // import arrayFrases from '../data/frases.json';

    export default {
        name: 'Escena',
        props: ['frases','currentSentence']
        // MUESTRA LOS DATOS DEL ARCHIVO JSON  
        // computed: {
        //     // método donde obtengo el array de frases con map
        //     obtenFrases() {
        //         return arrayFrases.map((item) => item)
        //     }
        // }
    }
</script>