
<script>



export default {
  name: "Card"
}
</script>

<template>
  <div class="card"> 
    <div>
      <img src="https://images.ygoprodeck.com/images/cards/652362.jpg" alt="">
    </div>
    <h3>name</h3>
    <h4>type</h4>
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