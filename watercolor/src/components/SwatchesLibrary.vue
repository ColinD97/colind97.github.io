<template>
  <div>
    <div class="library">
      <swatch-card v-for="card in $store.state.swatches" v-bind:key="card.NAME" v-bind:card="card"/>
    </div>
  </div>
</template>

<script>
import SwatchCard from "./SwatchCard.vue";
export default {
  name: "swatch-library",
  components: { SwatchCard },
};
</script>

<style>
.library {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  background-color: rgb(217, 237, 243);
  margin: 0 5rem 0 5rem;
}
</style>