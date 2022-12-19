<template>
    <v-row >
        <v-col cols="12" sm="6" style="text-align:center;padding:30vh 0 30vh 0">
            <span style="font-weight:900;font-size:40px">{{esquerre}}</span>
            <span style="font-weight:100;font-size:40px">{{dreta}}</span>
        </v-col>
        <v-col cols="12" sm="6">
            <Contacte
                class="pt-10"
                :titol="contacte.titol"
                :llista="contacte.llista"
            ></Contacte>
        </v-col>
    </v-row>
</template>

<script>
    export default{
        props:{
            esquerre:{
                type: String,
                default:"Muchas"
            },
            dreta:{
                type: String,
                default:"Gracias"
            },
            contacte:{
                type: String,
                default:""
            },
        }
    }

</script>