<template>
  <v-parallax src="http://www.brandgradients.com/img/backgrounds/instagram-hex-colors-gradient-background.png" height="450">
    <v-layout
      column
      align-center
      justify-center
      class="white--text"
    >
      <img src="~/assets/icon.png" alt="Vuetify.js" height="200">
      <h1 class="white--text mb-2 display-1 text-center">MooApp</h1>
      <div class="subheading mb-4 text-center">Controle sua produção em apenas alguns cliques</div>
      <v-btn class="mt-12" color="pink darken-1" dark align-left href="/">
        Conheça
      </v-btn>
    </v-layout>
  </v-parallax>
</template>

<script>
  export default {
    name: 'app-header',
    props: ['state']
  }
</script>