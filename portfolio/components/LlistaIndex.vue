<template>
    <v-row style="min-height:100vh">
       
        <v-col style="paddine-top:40vh" cols="12" md="4">
            <div class="elementIndex" v-for="(element, pos) in llista" :key="element.titol">
                <strong>
                    {{element.titol}}.
                </strong> 
                0{{pos + 1}}
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
    font-size: 30px;
    font-weight: 200;

}
</style>