<template>
    <section>
      <h1>Oops</h1>
      <nuxt-link to="/">Back to Home</nuxt-link>
    </section>
</template>

<script>
  export default {
    name: 'error'
  }
</script>

<style scoped>
  section {
    max-width: 600px;
    margin: 0 auto;
    padding-top: 5rem;
    color: red;
  }
</style>

