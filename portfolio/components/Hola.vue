<template>
    <v-row style="min-height:100vh" align="center">
        <v-col cols="12" sm="6" style="background:black">
            <v-img :src="imatge" style="position: relative"></v-img>
        </v-col>
        <v-col cols="12" sm="6" >
            <span style="font-size:80px;line-height:1em" v-html="titol"></span><br>
            <span >{{subTitol}}</span>
        </v-col>
    </v-row>
</template>
<script>
export default {
    props:{

        imatge:{
            type: String,
            default:""
        },
        titol:{
            type: String,
            default:"Hola soy <br> Andrey"
        },
        subTitol:{
            type: String,
            default:"Desiñadora Grafica"
        },
    }
    
}
</script>
