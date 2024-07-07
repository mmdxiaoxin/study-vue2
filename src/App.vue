<template>
  <div id="app">
    <BasicComponents />
    <DivideLine />
    <ListRender />
    <DivideLine />
    <StyleBind />
  </div>
</template>

<script>
import BasicComponents from "./components/BasicComponents.vue";
import DivideLine from "./components/DivideLine.vue";
import ListRender from "./components/ListRender.vue";
import StyleBind from "./components/StyleBind.vue";

export default {
  name: "App",
  components: {
    BasicComponents,
    DivideLine,
    ListRender,
    StyleBind,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
