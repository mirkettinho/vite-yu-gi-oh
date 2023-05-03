
<script>



export default {
  name: "Card",
  props:{
    name: String,
    type: String,
    img: Object
  }
}
</script>

<template>
  <div class="card"> 
    <div>
      <img :src="img.image_url" :alt="image">
    </div>
    <h5>{{name}}</h5>
    <h6>{{type}}</h6>
  </div>
</template>

<style lang="scss" scoped>

@use "../scss/partials/vars" as *;
.card{
  height: 380px;
  text-align: center;
  background-color: $primary-color;
  width: calc(100% / 6);
  margin-bottom: 30px;
  
  div{
  height: 300px;
  }
}
</style>