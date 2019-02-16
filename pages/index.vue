<template>

  <component :is="$store.state.mobile ? 'div': 'v-container'">

  </component>

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
