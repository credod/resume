<template>
  <div class="d-flex flex-column mb-4">
    <h6 class="m-0 mb-1 font-weight-bold text-theme">{{title}}</h6>
    <SectionItem
      v-for="(sectionItem, index) in sectionItems"
      :key="`${title}-${index}`"
      :item="sectionItem"
      :lastItem="index == sectionItems.length - 1"
    />
  </div>
</template>

<script>
import SectionItem from "./SectionItem";

export default {
  name: "Section",
  props: {
    title: String,
    sectionItems: Array,
  },
  components: {
    SectionItem,
  },
};
</script>
