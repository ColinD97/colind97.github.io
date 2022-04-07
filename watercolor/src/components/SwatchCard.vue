<template>
  <div class="card">
    <h4>{{card.color_name }}</h4>
    <p>CI Name: {{card.ci_name}}</p>
    <p>SKU: {{card.name}}</p>
    <p>Series {{card.series}}</p>
  </div>
</template>

<script>
export default {
    name: 'swatch-card',
    props: ['card'],
    data(){
        return {
            
        }
    }

}
</script>

<style>
.card {
  background-color: rgb(212, 212, 212);
  flex-basis: 10rem;
  margin: 1rem;
  border-radius: 0.5rem;
  box-shadow: 0.2rem 0.2rem 0.2rem rgb(196, 196, 196);
}
</style>