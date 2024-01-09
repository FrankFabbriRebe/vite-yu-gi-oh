<script>

// import axios
import axios from 'axios';

//import components
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

//import store
import { store } from './store'

export default {

  components: {
    AppHeader,
    AppMain,
  },

  data() {
    return {
      store,
    }
  },

  methods: {

    // call general api
    getCard() {
      axios
        .get(store.apiURL)
        .then((res => {
          // console.log(res.data);
          store.cardList = res.data.data
        }))
        .catch((err) => {
          console.log("Errors", err);
        })
    },

    // call api for archetype
    getArchetype() {
      axios
        .get(store.apiArchetype)
        .then((res => {
          // console.log(res.data);
          store.apiArchetype = res.data
        }))
        .catch((err) => {
          console.log("Errors", err);
        })
    }

  },

  created() {
    this.getCard(),
      this.getArchetype()
  }

}

</script>

<template>
  <AppHeader />
  <AppMain />
</template>

<style lang="scss">
// inclusion general.scss
@use "./style/general.scss"
</style>
