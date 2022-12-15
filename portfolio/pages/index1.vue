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
export default{
 
      data(){
    return{
      info:{
        titol:"Sobre mi",
        descripcio:"Ah, dear user of ChatGPT, thou art not alone in thy desire to engage with our esteemed AI chatbot. Many have flocked to our website in this hour, and we do our utmost to accommodate each and every one. Yet, alas, our resources are not without limit and we must ask for thy patience and forbearance. In time, we shall be able to provide thee with access to ChatGPT. Until then, we beg thee to return at a future juncture, when we may better serve thy needs. Until then, we bid thee adieu and good fortune.",
        competencia1:{
          titol:"Programacio",
          llista:[
            {
              text:"HTML",
              estrelles:4
            }
          ]
        },
        competencia2:{
          titol:"Idiomes",
          llista:[
            {
              text:"Català",
              estrelles:2
            }
          ]
        }
      }
    }
  }
}

</script>
