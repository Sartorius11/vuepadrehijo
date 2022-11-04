<template>
    <div>
        <h1 style="color:blue">
            {{ nombredeporte }}
        </h1>
        <button @click="selecionarFavorito">
            Seleccionar Favorito
        </button>

    </div>
</template>

<script>
export default{
    name:"HijoDeporte",
    props: ["nombredeporte"],
    methods:{
        selecionarFavorito(){
       
            //CUANDO  PULSEMOS EN EL HIJO, LLAMAMOS AL METODO
            //DEL PARENT QUE NOS HAN ENVIADO POR props
            this.$emit("seleccionarFavoritoParent","Su favorito es "+ this.nombredeporte);
        }
    },
    mounted(){
        console.log(this.nombredeporte);
    }
}
</script>



