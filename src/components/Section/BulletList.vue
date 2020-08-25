<template>
  <ul :class="`pl-4 ${lastItem ? 'm-0': ''}`">
    <li v-for="(item, index) in content" :key="index">{{item}}</li>
  </ul>
</template>

<script>
export default {
  name: "BulletList",
  props: {
    content: {
      type: Array,
      validator: (prop) => prop.every((e) => typeof e === "string"),
    },
    lastItem: {
      type: Boolean,
      default: false,
    },
  },
};
</script>