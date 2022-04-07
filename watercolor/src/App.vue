<template>
  <div id="app">
    <body>
      <head-bar />
      <sidebar-filter />
      <swatches-library />
    </body>
  </div>
</template>

<script>
import HeadBar from "./components/HeadBar.vue";
import SidebarFilter from "./components/SidebarFilter.vue";
import SwatchesLibrary from "./components/SwatchesLibrary.vue";

export default {
  name: "App",
  components: {
    SwatchesLibrary,
    HeadBar,
    SidebarFilter,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
body {
  display: grid;
}
</style>
