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
        :imatge="porfoliVue.hola.imatge"
    ></Hola>
    <Bio
        v-if="porfoliVue"
        :informacio="porfoliVue.bio"
        :informacioContacte="porfoliVue.bio"
    ></Bio>
    <LlistaIndex
    v-if="porfoliVue"
   :llista="porfoliVue.index.llista"
    ></LlistaIndex>
    <LlistaProjectes
    v-if="porfoliVue"
   :llista="porfoliVue.index.llista"
    ></LlistaProjectes>
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