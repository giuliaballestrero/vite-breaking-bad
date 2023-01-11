<script>

export default {
  data () {
    return {

    }
  }
}

</script>

<template>
  <section class="header-container">
    <img src="https://upload.wikimedia.org/wikipedia/commons/1/11/Yu-Gi-Oh%21_%28Logo%29.jpg" alt="yu-gi-oh logo">
    <h1>Yu-Gi-Uh Api</h1>
  </section>
</template>

<style lang="scss" scoped>
@use '../styles/general.scss' as *;
@use '../styles/partials/_variables.scss' as *;
.header-container {
  height: 150px;
  width: 100%;
  display: flex;
  align-items: center;

    img {
      padding: 2rem;
      height: 70%;
    }

    h1 {
      font-size: 4rem;
    }
}
</style>
