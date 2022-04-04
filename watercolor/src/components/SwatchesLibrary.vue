<template>
  <div>
    <div>
      <swatch-card v-for="card in $store.state.swatches" v-bind:key="card.NAME" v-bind:swatch="card"/>
    </div>
  </div>
</template>

<script>
import SwatchCard from "./SwatchCard.vue";
export default {
  components: { SwatchCard },
};
</script>

<style>
</style>