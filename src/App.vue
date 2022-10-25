<script>
import Directives from "./components/Directives.vue";
import EventHandling from "./components/EventHandling.vue";
import ListRender from "./components/ListRendering.vue";
import ConditionalRender from "./components/ConditionalRendering.vue";
export default {
  name: "App",
  components: { Directives, ConditionalRender, ListRender, EventHandling },
};
</script>

<template>
  <h1>Learning Vue</h1>
  <!-- <Directives /> -->
  <!-- <ConditionalRender /> -->
  <!-- <ListRender /> -->
  <EventHandling />
</template>

<style scoped></style>
