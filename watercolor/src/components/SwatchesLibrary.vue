<template>
  <div>
    <div class="library">
      <swatch-card
        v-for="card in this.$store.state.swatchesDisplay"
        v-bind:key="card.NAME"
        v-bind:card="card"
      />
        <!-- v-for="card in filterSwatches(this.fieldKey, this.$store.state.fieldValueName)" -->

    </div>
  </div>
</template>

<script>
import SwatchCard from "./SwatchCard.vue";
export default {
  name: "swatch-library",
  components: { SwatchCard },
  data(){
    return {
      fieldKey: 'series',
      value: 'Series 1'
    }
  },
  methods: {
    filterSwatches(field, value) {
      console.log(this.$store.state.swatches[0].color_name)
      return this.$store.state.swatches.filter((item) => {
        // return item[field] === value;
        return item[field] === 'Series 2' || value
      });
    },
  },
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