<template>
  <div>
    <div class="buttons">
      <Button
        v-for="caps in keyboards"
        v-bind:key="caps.id"
        v-bind:id="caps.id"
        v-bind:alph="caps.item"
        @remove="removeFromList(caps.id)" />
    </div>
  </div>
</template>

<script>
import Button from "./Button.vue";

export default {
  components: { Button },
  data() {
    return {
      keyboards: [
        { id: 1, item: "s" },
        { id: 2, item: "t" },
        { id: 3, item: "d" },
        { id: 4, item: "j" },
      ],
    };
  },
  methods: {
    removeFromList(id) {
      // console.log(id)

      this.keyboards = this.keyboards.filter((item) => item.id !== id);
    },
  },
};
</script>

<style scoped>
</style>
