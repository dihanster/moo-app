<template>
  <v-container grid-list-md text-xs-center>
    <v-card
      class="overflow-hidden"
      color="dark"
      light
    >
    <v-toolbar
      flat
      color="pink darken-1"
      dark
    >
      <v-toolbar-title  class="font-weight-dark">Cadastrar coleta</v-toolbar-title>
    </v-toolbar>

      <v-card-text>
        <v-text-field
          :disabled="!isEditing"
          color="black"
          label="Vaca"
        ></v-text-field>
        <v-autocomplete
          :disabled="!isEditing"
          :items="states"
          :filter="customFilter"
          color="black"
          item-text="name"
          label="Quantidade de leite coletado"
        ></v-autocomplete>
      </v-card-text>
      <v-divider></v-divider>
      <v-card-actions>
        <div class="flex-grow-1"></div>
        <v-btn
          :disabled="!isEditing"
          color="pink darken-1"
          @click="Salvar" 
          dark
        >
          Salvar
        </v-btn>
      </v-card-actions>
      <v-snackbar
        v-model="hasSaved"
        :timeout="2000"
        absolute
        bottom
        left
      >
      Atualizado!
      </v-snackbar>
    </v-card>
  </v-container>
</template>

<script>
  export default {
    data () {
      return {
        hasSaved: false,
        isEditing: true,
        model: null,
        states: [
        ],
      }
    },

    methods: {
      customFilter (item, queryText, itemText) {
        const textOne = item.name.toLowerCase()
        const textTwo = item.abbr.toLowerCase()
        const searchText = queryText.toLowerCase()

        return textOne.indexOf(searchText) > -1 ||
          textTwo.indexOf(searchText) > -1
      },
      save () {
        this.isEditing = !this.isEditing
        this.hasSaved = true
      },
    },
  }
</script>