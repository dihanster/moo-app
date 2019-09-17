<template>
  <div>
    <v-container grid-list-md text-xs-center>
      <todo-list/>
    </v-container>
  </div>
</template>

<script>
  import todo from '~/components/todo-list.vue'
  export default {
  	layout: 'default',
  	components: {
      'todo-list': todo
    },
    data: () => ({
    }),
  }
</script>

<style>
</style>