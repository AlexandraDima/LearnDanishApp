<template>
  <b-row class="pt-4">
      <b-col lg="4">
        <InfographicItem v-for="(item, index) in infographics" 
            :key="index" 
            :imagePath="item.url"
            :imageName="item.name"
        />
        </b-col>
  </b-row>
</template>

<script>
import InfographicItem from '../components/Infographic/InfographicItem'

export default {
    name: 'Infographics',
    components: {
        InfographicItem
    },
    data(){
        return {
            infographics : [
                {
                    url : 'Adverbs.svg',
                    name : 'Adverbs',
                },
                {
                    url : 'BodyHealth.svg',
                    name : 'Body parths'
                },
                {
                    url : 'FixedExpression.svg',
                    name : 'Fixed expressions'
                },
                {
                    url : 'Inversion.svg',
                    name : 'Inversion'
                },
                {
                    url : 'Numbers.svg',
                    name : 'Numbers'
                }
            ]
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
