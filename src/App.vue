<script>
  import AppHeader from './components/AppHeader.vue'
  import AppCards from './components/AppCards.vue'
  import AppMain from './components/AppMain.vue'
  import AppFooter from './components/AppFooter.vue'

  export default {
    components: {
      AppHeader,
      AppCards,
      AppMain,
      AppFooter,
    },
    data() {
      return {}
    },
  };
</script>

<template>
  <AppHeader />
  <AppCards />
  <AppMain />
  <AppFooter />
</template>

<style lang="scss"></style>