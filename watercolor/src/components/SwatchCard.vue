<template>
  <div>
    <h3>Name: {{card.color_name }}</h3>
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

</style>