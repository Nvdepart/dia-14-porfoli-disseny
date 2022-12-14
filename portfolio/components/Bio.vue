<template>
    <v-row style="height:100vh">
        <v-col cols="12" md="8">
            Text..
        </v-col>
        <v-col cols="12" md="4">
            <competencia style="color:aliceblue"
                titol="Idiomes"
            >
            </competencia>
            <competencia style="color:aliceblue"
                titol="Software"
            >
            </competencia>
        </v-col>
    </v-row>
</template>
<script>
    export default{
        data(){
            return {
                idiomes:[
                    {
                        text:"Rus",
                        estrelles:2
                    }
                ]
            }
        }
    }
</script>