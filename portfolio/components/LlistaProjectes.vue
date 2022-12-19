<template>
    <v-row style="min-height:100vh">
        <v-col style="paddine-top:40vh" cols="12" md="4">
            <div class="elementIndex" v-for="(projecte, pos) in llista" :key="projecte.titol">
                <div class="numeroGran">
                    0{{pos + 1}}
                </div> 
                <strong style="font-size:40px">
                    {{projecte.titol}}.
                </strong>
                <div v-for="(projecte,indexProjecte) in projecte.projectes" >
                    <projecte 
                    :projecte="projecte"
                    :numeroSeccio="pos"
                    :numeroProjecte="indexProjecte"
                    ></projecte>
                </div>
            </div>
       </v-col>
    </v-row>
</template>
<script>
    export default{
        props:["llista"]
    }
</script>

<style>
.elementIndex{
    font-weight: 200;
    min-height: 30px;
}
.numeroGran{
    font-size: 100px;
}
</style>