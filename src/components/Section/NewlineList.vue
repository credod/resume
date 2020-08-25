<template>
  <div>
    <p class="m-0" v-for="(item, index) in content" :key="index">{{item}}</p>
  </div>
</template>

<script>
export default {
  name: "NewlineList",
  props: {
    content: {
      type: Array,
      validator: (prop) => prop.every((e) => typeof e === "string"),
    },
  },
};
</script>