<template>
  <div>
    <div class="buttons">
      <Button
        v-for="caps in keyboards"
        :id="caps.id"
        :key="caps.id"
        :symbol="caps.item"
        @remove="removeFromList"
      />
    </div>
  </div>
</template>

<script>
import Button from './Button.vue'

export default {
  components: { Button },
  data () {
    return {
      keyboards: [
        { id: 1, item: 's' },
        { id: 2, item: 't' },
        { id: 3, item: 'd' },
        { id: 4, item: 'j' },
        { id: 5, item: 't' },
        { id: 6, item: 'd' },
        { id: 7, item: 'j' }
      ]
    }
  },
  methods: {
    removeFromList () {
      this.keyboards.shift()
    }
  }
}
</script>

<style scoped>
</style>
