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
        <img :src="card.card_images[0].image_url_small" :alt="card.name">
        <h3>{{ card.name }}</h3>
        <h4>{{ card.archetype }}</h4>
    </article>
</template>

<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/_variables.scss' as *;

</style>
