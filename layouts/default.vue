<template>
  <div>
    <div v-if="$auth.loggedIn">MENU</div>
    <nuxt />
  </div>
</template>

<script>
export default {
  data () {
    return {

    }
  },
  async created() {
    const cookie = await this.$axios.get('/csrf-cookie')
  }
}
</script>

<style scoped>

</style>
