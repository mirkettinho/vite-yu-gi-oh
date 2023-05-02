
<script>
export default {
  name: "Header"
}
</script>

<template>
  <header>
    <div class="vertical">
      <img src="../assets/img/pngegg.png" alt="logo ">
      <span>Yu-Gi-Oh Api</span>
    </div>
  </header>
</template>

<style lang="scss" scoped>

header{
  height: 40px;
  background-color: white;
  display: flex;
  padding-left: 10px;
}.vertical{
  display: flex;
  align-items: center;
  justify-content: center;
}span{
  color: black;
  padding-left: 10px;
}

</style>