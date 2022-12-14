<template>
    <div style="background:green">
        <h3>{{titol}}</h3>
        <!--
        <div v-for="(i,posicio) in 7">
            hola {{i}} - {{posicio}}
        </div>
        -->
        <div style="color:darkred" v-for="element in llista" :key="element.text">
            {{element.text}} :
            <span style="color:yellow" v-for="estrella in element.estrelles">
                * </span>
        </div>
    </div>
</template>
<script>
export default{
    props:{
        titol:{
            type:String,
            default:"Nom de la competència"
        },
        llista:{
            default:[
                {
                    text:"Català",
                    estrelles:3
                },
                {
                    text:"Castellà",
                    estrelles:3
                },
                {
                    text:"Anglès",
                    estrelles:5
                },
                {
                    text:"Francès",
                    estrelles:1
                },
            ]
        }
    }
}
</script>