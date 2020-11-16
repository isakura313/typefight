<template>
<button class="button is-link" @keydown[alph]="keyToDelete"> {{ alph }} </button>
</template>

<script>
export default {
  props: ["alph"],
  methods: {
    // keyToDelete () {
    //   this.$emit('remove', this)
    keyToDelete(event) {
      if (event.key === this.alph) {
        this.$emit("remove", data);
      }
    },
  },
};
</script>

<style scoped>
</style>
