<script>
import axios from 'axios';
import { store } from './store.js';
import MainApp from './components/MainApp.vue';
import HeaderApp from './components/HeaderApp.vue';

export default {
  components: {
    MainApp,
    HeaderApp,
  },

  data () {
    return {
      store,
    }
  },

  methods: {
    getCards (archetype) {
      console.log(archetype);
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=15&offset=0', {
        params: {
          archetype: archetype
        }
      })


      .then((response) => {
        console.log(response.data.data);
        this.store.cardList = response.data.data;
    })   
    }
  },

  created() {
    this.getCards();
  },
}

</script>

<template>
  <HeaderApp/>
  <MainApp @searchArchetype="getCards" />
</template>

<style lang="scss">

@use './styles/general.scss' as *;
@use './styles/partials/_variables.scss' as *;

</style>
