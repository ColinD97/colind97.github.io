<template>
  <div class="card">
    <h4>{{card.color_name }}</h4>
    <p>CI Name: {{card.ci_name}}</p>
    <p>SKU: {{card.name}}</p>
    <p>Series {{card.series}}</p>
    <p>{{colorNameToImgName()}}</p>
    <!-- <p>{{imagePath()}}</p> -->
    <!-- <img v-attr="colorNameToImgName" /> -->
    <img src='../assets/colors/azo_yellow.jpg'/>
    <!-- <img v:bind:src="colorNameToImgName" /> -->
    <img :src="colorNameToImgName()" />
  </div>
</template>

<script>
export default {
    name: 'swatch-card',
    props: ['card'],
    data(){
        return {
            
        }
    },
    computed: {
      // imagePath(){
      //   let cardName = this.card.color_name.toLowerCase().match(/[a-z]/g).join("")
      //   let imgName = this.$store.state.colorImg.find(element => {
      //     let nameNoJpg = element.substring(0,element.length-4)
      //     //nameNoJpg = nameNoJpg.match(/[a-z]g/)
      //     console.log(nameNoJpg)
      //     return nameNoJpg
      //     // .includes(cardName)
      //     })
      //   console.log("cardName: "+cardName + "  "+imgName)
      //   //imgName = this.$store.state.colorImg.find(element => )
      //   return cardName
      // }

    },
    methods: {
      colorNameToImgName(){
        let fileName = this.card.color_name.toLowerCase().replaceAll(' ', '_') + ('.jpg')
        fileName = ('../assets/colors/') + fileName
        return fileName
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