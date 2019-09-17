<template>
    <v-container grid-list-md text-xs-center>
      <v-toolbar
        flat
        color="pink darken-1"
        dark
      >
      <v-toolbar-title  class="font-weight-dark">Dashboard de Produção</v-toolbar-title>
      </v-toolbar>
      <br>
      <v-layout row wrap>        
        <v-flex v-for="(v, i) in values"
          :key="i" style="width: 700;" >
            <v-card
              class="mt-4 mx-auto"
              max-width="400"
            >
              <v-sheet
                class="v-sheet--offset mx-auto"
                :color="colors[i]"
                elevation="12"
                max-width="calc(100% - 32px)"
              >
                <v-sparkline
                  :labels="labels"
                  :value="v"
                  color="white"
                  line-width="4"
                  padding="16"
                  auto-draw-duration="2000"
                ></v-sparkline>
              </v-sheet>

              <v-card-text class="pt-0">
                <div class="title font-weight-light mb-2">{{titulos[i]}}</div>
              </v-card-text>
            </v-card>
        </v-flex> 
      </v-layout>
    </v-container>
</template>

<script>
  export default {
    data: () => ({
      labels: [
        '12am',
        '3am',
        '6am',
        '9am',
        '12pm',
        '3pm',
        '6pm',
        '9pm',
      ],
      colors: [
          'indigo',
          'warning',
          'pink darken-2',
          'red lighten-1',
          'deep-purple accent-4',
      ],
      titulos: [
        'Produção diária', 'Produção semanal', 'Produção mensal', 'Produção anual'
      ],
      values: [
        [
        200,
        675,
        410,
        390,
        310,
        460,
        250,
        240,
        ],
        [
          100,
          275,
          310,
          490,
          510,
          660,
          750,
          840,
        ],
        [
          100,
          275,
          310,
          490,
          510,
          660,
          750,
          840,
        ],
        [
          100,
          275,
          310,
          490,
          510,
          660,
          750,
          840,
        ],
      ],
    }),
  }
</script>

<style>
  .v-sheet--offset {
    top: -24px;
    position: relative;
  }
</style>