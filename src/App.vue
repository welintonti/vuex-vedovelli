<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1>Welcome Vue 2</h1>
    <h4> {{ user }} </h4>
  </div>
</template>

<script>
export default {
  name: 'app',
  computed: {
    user () {
      return `O usuário Logado é ${this.$store.state.user.name} e possui email ${this.$store.state.user.email}`
    }
  }
}
</script>
</style>
