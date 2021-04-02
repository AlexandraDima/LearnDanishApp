<template>
<!--   <b-row class="infographics__container pt-4">
        <InfographicItem ref="infographicItem" v-for="(item, index) in infographics" 
            :key="index" 
            :imagePath="item.url"
            :imageName="item.name"
        />
  </b-row> -->
    <div class="infographics_container">
        <InfographicItem ref="infographicItem" v-for="(item, index) in infographics" 
                    :key="index" 
                    :imagePath="item.url"
                    :imageName="item.name"
                />
    </div>
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
                    url : 'Adverbs2.svg',
                    name : 'Adverbs',
                },
                {
                    url : 'BodyHealth.svg',
                    name : 'Body parths'
                },
                {
                    url : 'FixedExpression2.svg',
                    name : 'Fixed expressions'
                },
                {
                    url : 'Inversion2.svg',
                    name : 'Inversion'
                },
                {
                    url : 'Numbers2.svg',
                    name : 'Numbers'
                },
                {
                    url : 'Adverbs2.svg',
                    name : 'Adverbs',
                },
                {
                    url : 'BodyHealth.svg',
                    name : 'Body parths'
                },
                {
                    url : 'Adverbs2.svg',
                    name : 'Adverbs',
                },
                  {
                    url : 'Numbers2.svg',
                    name : 'Numbers'
                },
            ]
        }
    },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.infographics_container {
   -webkit-column-count: 1;
    -moz-column-count:1;
    column-count: 1;
    -webkit-column-gap: 1rem;
    -moz-column-gap: 1rem;
    column-gap: 1rem;
    padding: 0;
    margin: 1rem;
}
@media only screen and (min-width: 900px){
    .infographics_container {
        -moz-column-count: 2;
        -webkit-column-count: 2;
        column-count: 2;
    }
}
@media only screen and (min-width: 1200px){
    .infographics_container {
        -moz-column-count: 3;
        -webkit-column-count: 3;
        column-count: 3;
    }
}
</style>
