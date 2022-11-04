<template>
    <div>
        <h1>Padre deportes</h1>
        <h1 style="color:red" v-if="favorito">
            {{favorito}}
        </h1>
        <ul>
            <li v-for="depor in deportes" :key="depor">
                <!-- se lo envio como propiedad al hijo  -->
                <HijoDeporte :nombredeporte="depor" 
                v-on:seleccionarFavoritoParent="seleccionarFavoritoParent"/>
            </li>
        </ul>

    </div>
</template>

<script>
import HijoDeporte from './HijoDeporte.vue';

export default{
    name:"PadreDeportes",
    components:{
        HijoDeporte
    },
    methods:{
        seleccionarFavoritoParent(nombre){
            console.log(nombre);
            this.favorito= nombre;

        }
    },
    data(){
        return{
            deportes:["Padel","Tenis","Balomano","Futbol","Fressbie","Peonza"],
            favorito:null

        }
    }
}
</script>



