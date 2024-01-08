<script>

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

export default {
  components: {
    AppHeader,
    AppMain,
  }
}

</script>

<template>
  <AppHeader />
  <AppMain />
  <AppCard />
</template>

<style lang="scss">
// inclusion general.scss
@use "./style/general.scss"
</style>
