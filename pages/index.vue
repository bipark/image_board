<template>

  <v-container>

  </v-container>

</template>

<script>


  export default {

    async asyncData({app, params, store, query}) {

      if (query.app) {
        store.commit("setApp", query.app);
      }

      return {
        page: params.page ? parseInt(params.page) : 1
      }
    },

  }
</script>

<style>
</style>
