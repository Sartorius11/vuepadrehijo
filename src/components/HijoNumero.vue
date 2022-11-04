<template>
    <div>
        <h1>Hijo Numero {{mandarNumero}}</h1>

            <button @click="numeroHijo">
                sumar
            </button>
    </div>

</template>

<script>
export default {
    name:"HijoNumero",
    props: ["mandarNumero"],
    methods:{
        numeroHijo(){
            this.$emit("sumarNumeros",this.mandarNumero)

        }
    }

    
}

</script>

<style >
    
</style>