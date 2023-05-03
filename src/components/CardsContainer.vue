<script>
import Card from "./Card.vue"
import { store } from "../data/store"


export default {
  name: "CardsContainer",
  components:{
    Card
  },
  data(){
    return{
      store
    }
  }
}
</script>

<template>
  <div class="container">
    <div class="foundCard">
      <span>Found {{ store.cardslist.length }} cards</span>
    </div>

    <div class="row">

      <Card v-for="card  in store.cardslist" :key="card"
      :img="card.card_images[0]" :name="card.name" :type="card.type"/>
    </div>
  </div>
</template>

<style lang="scss" scoped>

@use "../scss/partials/vars" as *;

.container{
  background-color: white;
  width: 90%;
  margin: 60px auto;
  
}.foundCard{
  background-color: $found-color;
  height: 50px;
}.row{
  display: flex;
  flex-wrap: wrap;
}
</style>