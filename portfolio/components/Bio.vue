<template>
    <v-row style="height:100vh">
        <v-col cols="12" md="8">
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
                   
                    :titol="informacio.c2.titol"
                    :llista="informacio.c2.llista"
                >
                </competencia>
    
                <Contacte
                    :titol="informacio.informacioContacte.titol"
                    :llista="informacio.informacioContacte.llista"
                ></Contacte>
        </v-col>
    </v-row>
</template>
<script>
    export default{

        props:['informacio','informacioContacte'],
        mounted(){
        console.log(this.info)
    }
}


</script>