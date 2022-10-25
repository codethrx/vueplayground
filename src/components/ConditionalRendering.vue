<template>
  <h1>ConditionalRender</h1>
  <p v-if="value === 0">The number is 0</p>
  <p v-else-if="value > 0">The number is +</p>
  <p v-else-if="value < 0">The number is -</p>
  <p v-else>Not a number..</p>

  <button @click="showHndl">{{ show ? "Collapese" : "Expand" }}</button>
  <p v-show="show">Lorem ipsum dolor sit amet.</p>
</template>
<script>
export default {
  data: () => ({
    value: "a",
    show: false,
  }),
  methods: {
    showHndl() {
      this.show = !this.show;
    },
  },
};
</script>
<style></style>
