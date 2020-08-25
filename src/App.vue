<template>
  <div id="app" class="page-text">
    <Page />
  </div>
</template>

<script>
import Page from "./components/Layout/Page.vue";

export default {
  name: "App",
  components: {
    Page,
  },
};
</script>

<style lang="scss">
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: rgb(82, 86, 89);
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100vw;
  height: 100vh;
}
</style>
