<template>
  <div>
    <button @click="mudarDados">Mudar dados do Usuário</button>
  </div>
</template>
<script>
  export default {
    methods: {
      mudarDados () {
        const payload = {
          name: 'Outro Nome',
          email: 'email@gmail.com',
          level: 5
        }
        this.$store.commit('CHANGE_USER', payload)
      }
    }
  }

</script>
