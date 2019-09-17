<template>
  <v-footer
    dark
    padless
    color="#f53b57"
  >
    <v-card
      class="flex"
      flat
      tile
      color="pink darken-1"
    >
    <!--
      <v-card-title>
        <strong class="subheading ">Fique ligado em nossas redes para mais novidades!</strong>

        <div class="flex-grow-1"></div>

        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4"
          dark
          icon
        >
          <v-icon size="24px">{{ icon }}</v-icon>
        </v-btn>
      </v-card-title>
	-->
      <v-card-actions class="grey darken-4 justify-center">
        {{ new Date().getFullYear() }} — <strong>MooApp</strong>
      </v-card-actions>
    </v-card>
  </v-footer>
</template>

