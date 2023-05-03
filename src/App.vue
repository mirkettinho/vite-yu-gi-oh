
<script>
import axios from "axios"
import Header from "./components/Header.vue"
import CardsContainer from "./components/CardsContainer.vue"
import SearchBar from "./components/SearchBar.vue"
import { store } from "./data/store"

export default {
  name: "App",
  data(){
    return{
      store
    }
  },
  components:{
    Header,
    CardsContainer,
    SearchBar
  },
  methods:{
    getApi(){
      axios.get(store.apiUrl)
      .then(result => {
        store.cardslist = result.data
        console.log(store.cardslist);
      })
    }
  },
  mounted(){
    this.getApi();
  }
}
</script>

<template>

  <Header/>
  <SearchBar/>
  <CardsContainer/>

</template>

<style lang="scss">

@use "./scss/main.scss";

</style>