<template>
  <h1>Basics - <span></span></h1>
  <p>Mustache Syntax -{{ name }}</p>
  <h4>Directives...</h4>
  <p v-text="name"></p>
  <p v-text="channel"></p>
  <p v-bind:id="headingId" v-text="channel"></p>
  <p>{{ btnStatus ? "Disable" : "Enable" }}</p>
  <button v-bind:disabled="btnStatus" @click="clickHandler">Click me...</button>
  <p v-bind:class="['danger', 'underline']">Adding name Classses</p>
  <p :class="[dangerClass, underlineClass]">Binding Class</p>
  <p :style="[inlineStyle1, inlineStyle2]">Inline Styles</p>
</template>
<script>
export default {
  data: () => ({
    name: "Directives Demo...",
    channel: "Binding data",
    htmlChunk: "<b>Binding html.</b>",
    headingId: "heading",
    btnStatus: false,
    dangerClass: "danger",
    underlineClass: "underline",
    inlineStyle1: {
      fontSize: "30px",
      fontWeight: "bold",
    },
    inlineStyle2: {
      background: "#23d997",
      color: "gray",
    },
  }),
  methods: {
    clickHandler() {
      this.btnStatus = !this.btnStatus;
    },
  },
};
</script>
<style scoped>
#heading {
  color: rgb(115, 8, 222);
}
.danger {
  color: red;
}
.underline {
  text-decoration: underline;
}
</style>
