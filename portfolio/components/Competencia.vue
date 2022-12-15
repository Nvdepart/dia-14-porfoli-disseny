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
            type:Array,
            default:[
                {
                    text:"text1",
                    estrelles:3
                },
                {
                    text:"text2",
                    estrelles:3
                },
                {
                    text:"text3",
                    estrelles:5
                },
                {
                    text:"text4",
                    estrelles:1
                },
            ]

        }
    }
}
</script>