<template>
  <b-container>
    <h1>page de connection</h1>
    <b-button @click="loginWith('google')">Google</b-button>
    <b-button @click="loginWith('facebook')">Facebook</b-button>
  </b-container>
</template>

<script>
  export default {
      auth: false,
      methods: {
          loginWith(provider) {
              this.$auth.loginWith(provider)
          }
      }
  };
</script>
