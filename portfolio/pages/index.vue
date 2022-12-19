<template>
<v-container>
    <!-- Importar dades del component d'inici-->
    <inici
        v-if="porfoliVue"
        :titolEsquerre="porfoliVue.inici.titolEsquerre"
        :titolDreta="porfoliVue.inici.titolDreta"
        :subTitol="porfoliVue.inici.subTitol"
        :nom="porfoliVue.inici.nom"
        :ofici="porfoliVue.inici.ofici"
  ></inici>
  <!-- Importar dades del component d'inici-->
    <Hola
    v-if="porfoliVue"
    :titol="porfoliVue.hola.titol"
    :subtitol="porfoliVue.hola.subtitol"
    :imatge="porfoliVue.hola.imatge"
  ></Hola>

    <Bio
        v-if="porfoliVue"
        :informacio="porfoliVue.bio"
    ></Bio>

    <LlistaIndex
    v-if="porfoliVue"
    :llista="porfoliVue.index.llista"
    ></LlistaIndex>

    <LlistaProjectes
    v-if="porfoliVue"
   :llista="porfoliVue.index.llista"
    ></LlistaProjectes>

    <Gracias  v-if="porfoliVue"
    :esquerre="porfoliVue.gracias.esquerre"
    :dreta="porfoliVue.gracias.dreta"
    :contacte="porfoliVue.bio.informacioContacte"
    ></Gracias>

</v-container>


</template>
<script>
import porfoli from "@/dades/porfoli"

export default {
    mounted() {
        this.porfoliVue = porfoli;
    },
    data() {
        return {
            porfoliVue: null
        };
    },
    
}

</script>