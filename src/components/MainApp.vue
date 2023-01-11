<script>
import { store } from '../store.js';
console.log(store);
import CardComponent from './CardComponent.vue';

export default {
  components:  {
    CardComponent,
  },

  data () {
    return {
      store,
    }
  },
}

</script>

<template>
  <section class="main-wrapper">

    <div class="menu-btn">
      <!--Qui andrà il menu a tendina... ma non è questo il giorno!-->
    </div>
    
    <div class="container">
      <div class="card-finder">
          <h2>Found {{ store.cardList.length }} cards</h2>
      </div>

      <div class="card-wrapper">
        <!--Qui andranno le card-->
      
        <CardComponent v-for="cardElement in store.cardList" 
        :card="cardElement"/>

      </div>
    </div>



  </section>
</template>

<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/_variables.scss' as *;
.main-wrapper {
  background-color: $main-bg-color;
  height: calc(100% - 300px);
}

.menu-btn {
  height: 150px;
  background-color: $main-bg-color;
}

.container {
  background-color: white;
  width: 80%;
  margin: auto;
}

.card-finder {
  background-color: $secondary-bg-color;
  padding: 2rem 0;
  color: white;
  border: 20px solid white;

    h2 {
      padding-left: 4rem;
    }
}

.card-wrapper {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}
</style>
