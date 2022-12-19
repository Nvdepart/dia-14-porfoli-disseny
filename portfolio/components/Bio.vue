<template>
    <v-row style="height:100vh">
        <v-col cols="12" md="8" class="BioCol">
            <h1>{{informacio.titol}}</h1>
            <p>{{informacio.descripcio}}</p>
        </v-col>
        
        <v-col cols="12" md="4" v-if="informacio">
                <competencia
                    
                    :titol="informacio.c1.titol"
                    :llista="informacio.c1.llista"
                >
                </competencia>
                <competencia
                    class="pt-10 idiomes"
                    :titol="informacio.c2.titol"
                    :llista="informacio.c2.llista"
                >
                </competencia>
    
                <Contacte
                class="pt-10"
                    :titol="informacio.informacioContacte.titol"
                    :llista="informacio.informacioContacte.llista"
                ></Contacte>
        </v-col>
    </v-row>
</template>
<script>
    export default{

        props:['informacio',],
        mounted(){
        console.log(this.info)
    }
}


</script>

<style scoped>
.bioCol{
    border-right: 1px solid rgb(58, 29, 29);
    padding-right:50px;
}
.idiomes{
    color:rgb(57, 211, 159)
}
</style>