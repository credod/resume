<template>
  <b-container class="p-0">
    <b-row class="m-0 w-100">
      <b-col class="p-0 w-100">
        <span class="name p-0 m-0">Credo Duarte</span>
      </b-col>
    </b-row>
    <b-row class="py-4 m-0 w-100">
      <ContactInfo />
    </b-row>
  </b-container>
</template>

<script>
import ContactInfo from "../ContactInfo/ContactInfo";
export default {
  name: "BasicInfo",
  components: {
    ContactInfo,
  },
};
</script>

<style>
</style>