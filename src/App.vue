<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1>Welcome Vue 2</h1>
    <h4> {{ user }} - {{ outraCoisa }}</h4>
    <hr>
    <AppUser />
  </div>
</template>

<script>
import AppUser from 'src/components/users/main.vue'
import { mapState, mapActions } from 'vuex'
export default {
  name: 'app',
  mounted () {
    const payload = {
      name: 'Welinton Subtil',
      email: 'welinton@realizati.com.br',
      level: 5,
      city: 'Porto Seguro',
      state: 'BA'
    }

    setTimeout(() => {
      this.changeUser(payload)
    }, 3000)
  },
  methods: {
    ...mapActions(['changeUser'])
  },
  components: {
    AppUser
  },
  computed: {
    ...mapState({
      user: state => {
        const { name, email } = state.user
        return `O usuário Logado é ${name} e possui email ${email}`
      }
    }),
    outraCoisa () {
      return 'Mais uma informação'
    }
  }
}
</script>
</style>
