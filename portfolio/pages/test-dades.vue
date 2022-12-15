<template>
    <div>
        Hola
        <v-icon color="blue">mdi-facebook</v-icon>
        <pre>
            {{porfoliVue}}
        </pre>
    </div>
</template>
<script>
import porfoli from "@/dades/porfoli.js"
console.log(porfoli)
export default{
    mounted(){
        this.porfoliVue = porfoli
    },
    data(){
        return{
            porfoliVue:{}
        }
    }
}
</script>