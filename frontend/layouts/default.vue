<template>
  <v-app class="app">
    <toolbar :state="layout"/>
    <v-content>
      <!--<v-container fluid>-->
        <nuxt></nuxt>
      <!--</v-container>-->
    </v-content>
    <header :state="layout"/>
    <le-footer/>
    <v-snackbar
      :timeout="snack.timeout"
      :color="snack.color"
      bottom
      v-model="snack.visible"
    >
      {{snack.text}}
      <v-btn dark flat @click.native="snack.visible = false">Close</v-btn>
    </v-snackbar>
  </v-app>
</template>

<script>
  import toolbar from '~/components/toolbar.vue'
  import sidenavLeft from '~/components/sidenav-left.vue'
  import sidenavRight from '~/components/sidenav-right.vue'
  import footer from '~/components/footer.vue'
  import header from '~/components/header.vue'

  export default {
    components: {
      toolbar,
      header,
      leFooter: footer
    },
    data: () => ({
      layout: {
        drawer: true,
      },
    }),
    computed: {
      snack () {
        return this.$store.getters.snack
      }
    }
  }
</script>