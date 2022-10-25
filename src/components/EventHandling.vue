<template>
  <h1>Event handling...</h1>
  <form>
    <input type="text" placeholder="name" v-model="formData.name" />
    <textarea placeholder="info" v-model="formData.info"></textarea>
    <select v-model="formData.status">
      <option value="resident">Resident</option>
      <option value="non-resident">Non Resident</option>
    </select>
    <!-- <label for="">Is eligible.</label> -->
    <input v-model="formData.isEligible" type="checkbox" />
    <button @click="showFormData">Show Form data</button>
  </form>
</template>
<script>
export default {
  data: () => ({
    formData: {
      name: "",
      info: "",
      status: "resident",
      isEligible: false,
    },
  }),
  methods: {
    showFormData(e) {
      e.preventDefault();

      console.log(this.formData.name);
    },
  },
};
</script>
