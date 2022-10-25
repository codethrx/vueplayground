<template>
  <h1>ListRende</h1>
  <p v-for="{ name, rating, id } in games" :key="id" @click="printName(id)">
    {{ name + " " + rating }}
  </p>
</template>
<script>
import { generateUid } from "../utils/uid";
export default {
  data: () => ({
    games: [
      { name: "Fortknight", rating: 8, id: generateUid() },
      { name: "COD", rating: 10, id: generateUid() },
      { name: "GTA V", rating: 7, id: generateUid() },
    ],
  }),
  methods: {
    printName(name) {
      console.log(name);
    },
  },
};
</script>
<style></style>
