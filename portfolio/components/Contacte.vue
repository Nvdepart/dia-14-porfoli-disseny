<template>
    <div>
        <h1>{{titol}}</h1>
        <div style="color:darkred" 
            v-for="element in llista" 
            :key="element.icona">
            <v-icon color="blue">{{element.icona}}</v-icon> : {{element.text}}
        </div>
    </div>
</template>
<script>
    export default{
        props:{
    llista:{
        type:Array,
        required:true
    },
    titol:{
        type:String,
        default:"Contacto"
    }
   }
}
</script>