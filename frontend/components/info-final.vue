<template>
  <center>
  <v-flex xs12 >
            <v-container grid-list-xl >
              <v-card-title primary-title class="layout justify-center">
                  <div class="headline text-center">Gostou? Contate-nos</div>
                </v-card-title>
              <v-layout row wrap align-center>
                <v-flex xs12 md4>
                  <v-card flat class="transparent">
                    <v-card-text class="text-center">
                    <center> 
                      <img height="36px" align-center src="~/assets/contato.png"></center>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline text-center">Contato</div>
                    </v-card-title>
                    <v-card-text> (12) 1234-0000 | mooapp@gmail.com </v-card-text>
                  </v-card> 
                </v-flex>
              <img src="~/assets/contato.jpg" alt="Vuetify.js" height="250">
              </v-layout>
            </v-container>
  </v-flex>
  </center>
</template>

<script>
  export default {
    data: () => ({
      cards: [
       { title: 'Contato', txt: 'Com o MooAPP você tem todas as informações importantes de suas vacas leiteiras e produção de leite com apenas alguns cliques.'},
      ],
    }),
  }
</script>