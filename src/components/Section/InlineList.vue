<template>
  <div>
    <span v-for="(item, index) in content" :key="index">{{index != 0 ? ` ○ ${item}` : item}}</span>
  </div>
</template>

<script>
export default {
  name: "InlineList",
  props: {
    content: {
      type: Array,
      validator: (prop) => prop.every((e) => typeof e === "string"),
    },
  },
};
</script>