<template>
  <div class="infographicItem_container">
    <img :src="require(`@/assets/Infographics/${imagePath}`)" />
    <div class="row">
    <div class="col-lg-6">
    <p>{{imageName}}</p>
    </div>
    <div class="col-lg-6"> 
    <span>Likes: {{imageLikes}}</span>
    </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'InfographicItem',
  props: {
    imagePath: String,
    imageName: String,
    imageLikes: Number
  }
}
</script>

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
