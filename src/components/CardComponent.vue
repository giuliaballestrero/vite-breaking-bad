<script>
import { store } from '../store.js';

export default {
  
    props: {
        card: Object,
    },

    data () {
    return {
        store,
    }
    }
}

</script>

<template>
    <article class="single-card" :data-custom-id="card.id">
        <img :src="card.card_images[0].image_url" :alt="card.name">
        <h3>{{ card.name }}</h3>
        <h4>{{ card.archetype }}</h4>
    </article>
</template>

<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/_variables.scss' as *;

.single-card {
    width: calc(100% / 5 - 4rem);
    margin: 2rem;
    background-color: $main-bg-color;

    img {
        width: 100%;
    }

    h3 {
        text-transform: uppercase;
        color: white;
        text-align: center;
        font-size: 1.5rem;
        padding: 1rem;
    }

    h4 {
        font-size: 1.3rem;
        text-align: center;
        padding: 1rem;
    }
}

</style>
