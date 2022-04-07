<template>
  <div id="app">
    <body>
      <header>
        <head-bar />
      </header>
      <main>
        <swatches-library />
      </main>
      <aside>
        <sidebar-filter />
      </aside>
      <footer>footer</footer>
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
  grid-template-columns: 100px 90vw;
  grid-template-areas:
    "header header"
    "aside main"
    "footer footer";
}
header {
  /* color: rebeccapurple; */
  background-color: darkolivegreen;
  grid-area: header;
}
main {
  grid-area: main;
}
aside {
  background-color: bisque;
  grid-area: aside;
}
footer {
  background-color: darkseagreen;
  grid-area: footer;
}
</style>
