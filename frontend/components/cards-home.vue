<template>
    <v-container grid-list-md text-xs-center>
      <v-layout row wrap>        
        <v-flex v-for="card in cards"
          :key="card.title"
          :cols="card.flex" style="width: 700;">
          <v-card
            class="mx-auto"
            max-width="700"
            :to = card.caminho
          >
            <v-img
                class="white--text"
                height="200px"
                :src=card.src
              >
            </v-img>
            <v-card-title class="title" v-text="card.title"></v-card-title>
            <!--<v-btn depressed small dark color="#f53b57" :to=card.caminho>Ver mais</v-btn>-->
          </v-card>
        </v-flex> 
      </v-layout>
    </v-container>
</template>

<script>
  export default {
    data: () => ({
      cards: [
        { title: 'Listas', src: 'https://cdn1.vectorstock.com/i/1000x1000/03/95/milk-cow-concept-banner-flat-style-vector-26240395.jpg', flex: 12, caminho : "lista" },
        { title: 'Produção', src: 'https://st2.depositphotos.com/1967477/6345/v/950/depositphotos_63454695-stock-illustration-happy-cartoon-cow.jpg', flex: 6, 
          caminho : "producao" },
        { title: 'Analytcs', src: 'https://ak3.picdn.net/shutterstock/videos/4758293/thumb/1.jpg', flex: 6,
        caminho : "analytcs" },
        { title: 'Tarefas', src: 'https://i.gifer.com/KhAX.gif', flex: 6, caminho : "tarefas" },

      ],
    }),
  }
</script>