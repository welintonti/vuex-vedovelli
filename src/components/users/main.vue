<template>
  <div>
    Email: {{ email }}
    <br>
    Localidade: {{ localidade }}
    <AppButton></AppButton>
  </div>
</template>
<script>
  import AppButton from '../button'
  import { mapGetters } from 'vuex'
  export default {
    components: {
      AppButton
    },
    computed: {
      email () {
        return this.$store.state.user.email
      },
      ...mapGetters([
        'localidade'
      ])
    }
  }

</script>
