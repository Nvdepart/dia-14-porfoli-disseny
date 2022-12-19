<template>
       
    <div v-if="projecte">
        <h3>{{projecte.titol}}</h3>
        <p style="max-width:500px; text-align:justify; text-justify:inter-word">{{projecte.text}}</p>
        <nuxt-link
        :to="'/projectes/'+numeroSeccio+'/'+numeroProjecte"
        >veure projecte</nuxt-link>
        <v-row>
            <v-col cols="4" v-for="imatge in projecte.imatges">
                <v-img  
                aspect-ratio="1"
                :src="imatge">
                {{numeroSeccio}} / {{numeroProjecte}}
                </v-img>
            </v-col>
        </v-row>
    </div>

</template>

<script>
export default {
    props:["projecte","numeroSeccio","numeroProjecte"]
    
}
</script>