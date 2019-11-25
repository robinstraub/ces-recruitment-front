<template>
  <div>
    <div>
      <b-navbar type="dark" variant="primary">
        <b-navbar-brand href="#">CES Recruitment</b-navbar-brand>
        <b-navbar-nav class="ml-auto" v-if="$auth.loggedIn">
          <b-nav-item-dropdown :text="$auth.user.name" right>
            <b-dropdown-item @click="logout">Se déconnecter</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-navbar>
    </div>
    <nuxt />
  </div>
</template>

<script>
  export default {
      methods: {
          logout() {
              return this.$auth.logout()
          }
      }
  };
</script>
