<template>

    <div v-if="profoliSelecionat" >
        <v-row>
            <v-col cols="6" class="pa-4">
                <h1>{{profoliSelecionat.titol}}</h1>
                <nuxt-link
                    :to="'/'"
                     >Tournar  l'inici
                </nuxt-link>
            </v-col>
            <v-col cols="6">
                <p style="max-width:500px  text-align:center text-justify:center">
                 {{profoliSelecionat.text}}
                </p>
            </v-col>
            <v-col cols="12" >
                    <v-img  v-for="imatge in profoliSelecionat.imatges"
                    aspect-ratio="1"
                    :src="imatge"
                    class="mb-5 ma-10"
                    style="border-radius:50%"
                    ></v-img>
            </v-col>
        </v-row>
    </div>
</template>

<script>
import porfoli from '@/dades/porfoli.js'
export default{
    mounted(){
        let categoria = this.$route.params.categoria
        let projecte = this.$route.params.projecte
        console.log(categoria.projecte)
        console.log(porfoli.index.llista[categoria].projectes[projecte])
        this.profoliSelecionat = porfoli.index.llista[categoria].projectes[projecte]
    },
    data(){
        return {
            profoliSelecionat: null
        }
    }
}
</script>