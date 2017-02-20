<template>
  <div>
    <button :disabled="!hasUser" @click="mudarDados">Mudar dados do Usuário</button>
  </div>
</template>
<script>
  import { mapState, mapActions } from 'vuex'
  export default {
    methods: {
      mudarDados () {
        const payload = {
          name: 'Outro Nome',
          email: 'email@gmail.com',
          level: 5,
          city: 'Porto Seguro',
          state: 'BA'
        }
        this.changeUser(payload)
        // this.$store.commit('CHANGE_USER', payload)
      },
      ...mapActions(['changeUser'])
    },
    computed: {
      ...mapState({
        hasUser: state => state.user.name !== ''
      })
    }
  }

</script>
