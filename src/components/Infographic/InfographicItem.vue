<template>
  <div>
    <img :src="require(`@/assets/Infographics/${imagePath}`)" />
    <p>{{imageName}}</p>
  </div>
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
<style scoped>

</style>
