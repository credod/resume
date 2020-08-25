<template>
  <b-container class="p-0">
    <b-row class="m-0">
      <IconSpan :icon="['fas', 'envelope']" text="credo_duarte@brown.edu" />
    </b-row>
    <b-row class="m-0">
      <IconSpan :icon="['fas', 'phone']" text="(312) 945 9539" />
    </b-row>
    <b-row class="m-0">
      <IconSpan :icon="['fab', 'github']" text="credod" />
    </b-row>
    <b-row class="m-0">
      <IconSpan :icon="['fas', 'map-marker-alt']" text="Chicago, IL" />
    </b-row>
  </b-container>
</template>

<script>
import IconSpan from "./IconSpan";
export default {
  name: "ContactInfo",
  components: {
    IconSpan,
  },
};
</script>

<style>
</style>