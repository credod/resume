<template>
  <div v-if="!!item">
    <div class="d-flex justify-content-between align-items-center">
      <span class="font-weight-bold">{{item.itemTitle}}</span>
      <span class="text-right">{{item.date}}</span>
    </div>
    {{item.subtitle}}
    <InlineList v-if="item.listType === 'inlineList'" :content="item.listItems" />
    <NewlineList v-else-if="item.listType === 'newlineList'" :content="item.listItems" />
    <BulletList
      v-else-if="item.listType === 'bulletList'"
      :content="item.listItems"
      :lastItem="lastItem"
    />
  </div>
</template>

<script>
import InlineList from "./InlineList";
import NewlineList from "./NewlineList";
import BulletList from "./BulletList";

export default {
  name: "SectionItem",
  props: {
    item: {
      itemTitle: String,
      date: String,
      subtitle: String,
      listType: {
        type: String,
        validator: (prop) =>
          ["bulletList", "inlineList", "newlineList"].includes(prop),
      },
      listItems: {
        type: Array,
        validator: (prop) => prop.every((e) => typeof e === "string"),
      },
    },
    lastItem: {
      type: Boolean,
      default: false,
    },
  },
  components: {
    InlineList,
    NewlineList,
    BulletList,
  },
};
</script>