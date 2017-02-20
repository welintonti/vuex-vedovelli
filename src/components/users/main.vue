<template>
  <div>
    Email: {{ email }}
    <AppButton></AppButton>
  </div>
</template>
<script>
  import AppButton from '../button'
  export default {
    components: {
      AppButton
    },
    computed: {
      email () {
        return this.$store.state.user.email
      }
    }
  }

</script>
