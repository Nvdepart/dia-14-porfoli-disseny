<template>
    <v-row style="min-height:100vh" align="center">
        <v-col cols="6" sm="6" style="background:black">
            <v-img :src="imatge" :aspect-ratio="1/2"></v-img>
        </v-col>
        <v-col cols="6" sm="6" >
            <span class="titolGran" v-html="titol"></span><br>
            <span >{{subTitol}}</span>
        </v-col>
    </v-row>
</template>
<script>
    export default {
        props:{

            imatge:{
                type: String,
                default:"https://images.pexels.com/photos/1561020/pexels-photo-1561020.jpeg"
            },
            titol:{
                type: String,
                default:"<strong>Hola</strong> soy <br> <strong>Andrea</strong>"
            },
            subTitol:{
                type: String,
                default:"Desiñadora Grafica"
            },
        }   
    }
</script>

<style scoped>
.titolGran{
    font-size:80px;
    line-height:1em;
    background-color:rgb(146, 136, 136);
}
@media screen and (max-width: 800px) {
    .titolGran{
        font-size:60px;
        background-color:rgb(90, 90, 98);
    }
}
@media screen and (max-width: 480px) {
    .titolGran{
        font-size:40px;
        background-color:rgb(88, 108, 88);
       
    }
}
</style>
