<template>
    <Benvinguda @cambia="cambiaInici" v-if="!btnInici"></Benvinguda>
    
    <div v-if="btnInici">   
        <Botons @accio="accionBtn"></Botons>
        <Escena :frases="frases" :currentSentence="currentSentence"></Escena> 
    </div>


</template>

<script>
    import Benvinguda from './Benvinguda.vue'
    import Botons from './Botons.vue'
    import Escena from './Escena.vue'

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
              console.log(this.btnInici);
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
                frases: [
                "El nostre heroi estava surant per l'espai sideral quan a la llunyania va albirar una nau espacial",
                "Sentia curiositat per l'interior de la nau i es va posar a inspeccionar-la. Va arribar a una sala amb dues portes.",
                "L'heroi va decidir travessar la porta que el portava a casa",
                "Mentrestant, altres herois no van tenir tanta sort en la seva elecció ..."
                ]
            }            
        }
    }
</script>