<template>
    <div>
        <h3>{{titol}}</h3>
        <div v-for="element in llista" :key="element.text">
            {{element.text}} - 
            <span v-for="estrella in element.estrelles">
                {{estrella}}</span>
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