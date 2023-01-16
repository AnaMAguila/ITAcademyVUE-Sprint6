<template>
    <div>
        <!-- Dejo las dos formas de leer el array: -->
        <!-- MUESTRA LOS DATOS DEL DATA HOME.VUE -->
        <ul>
            <li v-for="text in frases" :key="text">
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
        props: ['frases']
        // MUESTRA LOS DATOS DEL ARCHIVO JSON  
        // computed: {
        //     // método donde obtengo el array de frases con map
        //     obtenFrases() {
        //         return arrayFrases.map((item) => item)
        //     }
        // }
    }
</script>

<!-- Hojas de estilo en carpeta css/style.css -->
<!-- <style>
    ul {
        list-style: none;
        margin : 0;
        padding: 0;
    }

    li {
        margin: 15px;
        padding: 15px;
        text-align: center;
        border: 2px solid #000;
        border-radius: 30px;
        background-color: #fff;
    }
</style> -->