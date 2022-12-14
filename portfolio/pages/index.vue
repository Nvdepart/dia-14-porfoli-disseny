<template>
  <v-container>
      <Inici
        titolEsquerre="Port"
        titolDreta="folio."
        subTitol="-------------------------------------------------------2019-2022"
        nom="Andrea López"
        ofici="Diseño Gráfico"
      ></Inici>
      <Hola
      imatge="https://cdn.pixabay.com/photo/2022/12/06/06/21/lavender-7638368_960_720.jpg"
      titol="<strong>Hola</stronge>, Soy <br> <strong>Andrea</stronge>"
      subTitol="Desiñadora Grafica"
      ></Hola>
      <bio :informacio="info"></bio>
      
  </v-container>
</template>

<script>
export default {
  data(){
    return{
      info:{}
    }
  }
}
</script>
