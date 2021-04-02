<template>
  <div class="infographicItem_container">
    <img :src="require(`@/assets/Infographics/${imagePath}`)" />
    <p>{{imageName}}</p>
  </div>
  <!--  <b-col lg="4" class="infographicItem_container">
    <img :src="require(`@/assets/Infographics/${imagePath}`)" />
    <p>{{imageName}}</p>
  </b-col> -->
</template>

<script>
export default {
  name: 'InfographicItem',
  props: {
    imagePath: String,
    imageName: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.infographicItem_container {
    display: inline-block;
    background: #fff;
    padding: 0.5em;
    margin: 0 0 1.5em;
    width: 100%;
    box-sizing: border-box;
    -moz-box-sizing: border-box;
    -webkit-box-sizing: border-box;
    box-shadow: 2px 2px 4px 0 #ccc;

    img {
      max-width:100%; height: auto;
      }
}

</style>
