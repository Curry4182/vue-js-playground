<template>
  <div>
    <AppHeader :title="appTitle" v-on:change="changeAppTitle"></AppHeader>
  </div>
</template>

<script>
  import AppHeader from './components/AppHeader.vue';
  export default {
    components: {
      AppHeader
    },
    data() {
      return {
        appTitle: 'App New Title'
      }
    },
    methods: {
      changeAppTitle() {
        this.appTitle = 'Changed New Title'
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>