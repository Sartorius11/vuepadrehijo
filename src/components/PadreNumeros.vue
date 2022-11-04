<template>
    <div>
        <h1> Padre Numeros </h1>

        <h1>La suma es : {{totalNumeros}} </h1>

        <button @click="sacarHijo">
            pulsa
        </button>

        <ul>
            <li v-for="Random in numeros" :key="Random">
                  <HijoNumero :mandarNumero="Random" v-on:sumarNumeros="sumarNumeros"></HijoNumero>
            
                    
            </li>   
        </ul>

        
        
    </div>
</template>

<script>
import HijoNumero from './HijoNumero.vue';
export default {
    name:"PadreNumeros",
    components:{
        HijoNumero
    },

    methods:{
            sacarHijo(){
              
                var NumerosRandom= parseInt(Math.random() * (100 - 1) + 1);

                this.numeros.push(NumerosRandom);
            },

            sumarNumeros(numeroHijo){
                console.log("asdfsadf");

                this.totalNumeros+=numeroHijo;





            }
           

        },




    data(){
        return{
            numeros:[],

            totalNumeros:0


        }
    }

}
</script>

<style>
    
</style>