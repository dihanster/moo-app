<template>
  <v-flex xs12 >
            <v-container grid-list-xl >
                <v-card-title primary-title class="layout justify-center">
                  <div class="headline text-center">Conheça o MooApp</div>
                </v-card-title>
              <v-layout row wrap align-center>
                <v-flex xs12 md4 v-for="card in cards" :key="card.title">
                  <v-card flat class="transparent">
                    <v-card-text class="text-center">
                    <center> 
                    <img height="36px" align-center :src=card.src>
                    </center>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline text-center">{{card.title}}</div>
                    </v-card-title>
                    <v-card-text> {{card.txt}} </v-card-text>
                  </v-card>
                </v-flex>              
              </v-layout>
            </v-container>
            <v-card-title primary-title class="layout justify-center">
                <div class="headline text-center">Veja o que oferecemos</div>
            </v-card-title>
          </v-flex>
</template>

<script>
  export default {
    data: () => ({
      cards: [
       { title: 'Prático', txt: 'Com o MooAPP você tem todas as informações importantes de suas vacas leiteiras e produção de leite com apenas alguns cliques.', src: 'https://i.imgur.com/w9pJJ2z.png'},
        { title: 'Intuítivo', txt: 'Todas as funcionalidades são simplificadas, de fácil acesso e de interpretação.', src: 'https://i.imgur.com/f7584SN.png'},
        { title: 'Eficiente', txt: 'Em apenas alguns instantes, toda a informação é processada e armazenada.',
          src: 'https://i.imgur.com/bvcdAw5.png'}
      ],
    }),
  }
</script>