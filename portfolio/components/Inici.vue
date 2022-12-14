<template>
    <v-row style="height:100vh" align="center">
        <v-col cols="12" sm="6" style="background:green">
            <span class="esquerre">{{titolEsquerre}}</span>
            <span class="dreta">{{titolDreta}}</span>
            <div style="line-height:0.1">{{subTitol}}</div>
            <div style="padding-top:20vh">
                <span class="textBaix">{{nom}}</span><br>
                <span class="textBaix">{{ofici}}</span>
            </div>  
        </v-col>
    </v-row>
</template>
<script>
export default{
    mounted(){
        console.log(this.titolEsquerre)
    },
    props:[
        'titolEsquerre',
        'titolDreta',
        'subTitol',
        'nom',
        'ofici'
    ]
}
</script>

<style scoped>
.esquerre{
    color:azure;
    font-size:80px;
    font-weight: 900;
}
.dreta{
    color:rgb(42, 26, 190);
    font-size:80px;
    font-weight: 100;
}
.textBaix{
    font-size:20px;
    font-weight: 900;
}

</style>