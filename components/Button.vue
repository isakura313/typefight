<template>
  <button class="button is-link" @keydown="keyToDelete">
    {{ symbol }}
  </button>
</template>

<script>
export default {
  props: {
    symbol: {
      type: String,
      default: 'A'
    }
  },
  created () {
    // eslint-disable-next-line nuxt/no-globals-in-created
    window.addEventListener('keydown', (e) => {
      if (e.key === this.symbol) {
        this.$emit('remove')
      }
    })
  }
}
</script>

<style scoped>
</style>
