<template>
  <b-row class="m-0 w-100">
    <b-col cols="1" class="p-0 text-center">
      <icon :icon="icon" />
    </b-col>
    <b-col cols="11" class="p-0 pl-1">
      <span>{{text}}</span>
    </b-col>
  </b-row>
</template>

<script>
export default {
  name: "IconSpan",
  props: {
    icon: {
      type: Array,
      validator: (prop) => prop.every((e) => typeof e === "string"),
      required: true,
    },
    text: String,
  },
};
</script>