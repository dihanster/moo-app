<template>
  <div>
    <app-header/>
    <!--<app-slides/>-->
    <banner/>
    <app-cards/> 
    <info/>
    <br> <br> <br>
  </div>
</template>

<script>
  import header from '~/components/header.vue'
  import card from '~/components/cards-home.vue'
  import slides from '~/components/slide.vue'
  import banner from '~/components/banner-info.vue'
  import info from '~/components/info-final.vue'
  export default {
  	layout: 'default',
  	components: {
      'app-header': header,
      'app-cards': card,
      'app-slides': slides,
      'banner': banner,
      'info': info
    },
    data: () => ({
    }),
  }
</script>

<style>
</style>
