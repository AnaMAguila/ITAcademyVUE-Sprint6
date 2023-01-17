<template>
    <Benvinguda @cambia="cambiaInici" v-if="!btnInici"></Benvinguda>

    <div :style="{backgroundImage:`url(${arrayFrases[currentSentence].img})`}" v-if="btnInici" class="fondo">  
        <Botons @accio="accionBtn"></Botons>
        <Escena :arrayFrases=arrayFrases :currentSentence="currentSentence"></Escena> 
    </div> 
</template>

<script>
    import Benvinguda from './Benvinguda.vue'
    import Botons from './Botons.vue'
    import Escena from './Escena.vue'
    import {arrayFrases} from '../data/frases.js'

    export default {
        name: 'Home',
        components: {
            Benvinguda,
            Botons,
            Escena
        },
        methods: {
            cambiaInici(posicion){
              this.btnInici = posicion;
              return this.btnInici; 
            },
            accionBtn(event){
                if(!event){
                    if(this.currentSentence>0){
                        this.currentSentence--;
                    }else if(this.currentSentence<0){
                        this.currentSentence = 0;
                    }
                } else {
                    if(this.currentSentence<3){
                        this.currentSentence++;
                    }else if(this.currentSentence>3){
                        this.currentSentence = 3;
                    }
                } 
            }          
        },
        data() {
            return {
                btnInici: 0,
                currentSentence: 0,
                arrayFrases: arrayFrases                
            }            
        }
    }
</script>