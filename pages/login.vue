<template>
    <section>
      <div class="alert alert-danger mb-3" v-if="$route.query.message">Do login first</div>
      <form @submit.prevent="onSubmit">
        <h1>Login page</h1>
        <div class="form-group">
          <input type="text" class="form-control">
        </div>
        <p>
          <nuxt-link to="/">Back to Home</nuxt-link>
        </p>
        <button class="btn btn-primary" type="submit">Do Login</button>
      </form>
    </section>
</template>

<script>
  export default {
    name: 'login',
    layout: 'clean',
    methods: {
      onSubmit() {
        this.$store.dispatch('login')
        this.$router.push('/')
      }
    }
  }
</script>

<style scoped>
  section {
    max-width: 500px;
    margin: 0 auto;
  }
</style>
