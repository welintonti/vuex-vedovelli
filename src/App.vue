<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1>Welcome Vue 2</h1>
    <h4> {{ user }} </h4>
    <hr>
    <AppUser />
  </div>
</template>

<script>
import AppUser from 'src/components/users/main.vue'
export default {
  name: 'app',
  components: {
    AppUser
  },
  computed: {
    user () {
      const { name, email } = this.$store.state.user
      return `O usuário Logado é ${name} e possui email ${email}`
    }
  }
}
</script>
</style>
