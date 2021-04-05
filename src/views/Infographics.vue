<template>
    <div>
        <div class="row col-lg-12 mt-3">
            <select class="col-lg-6 mx-auto" v-model="category">
            <option v-for="item in categories" 
                    :key="item.id" :value="`${item.name}`">{{item.name}}</option>
            </select> 
             <span :class="getButtonClass"><strong>{{ category }}</strong></span>
        </div>
       
        <div class="infographics_container">
            <InfographicItem ref="infographicItem" v-for="(item, index) in filterByCategory" 
                        :key="index" 
                        :imagePath="item.url"
                        :imageName="item.tags"
                        :imageLikes="item.likes"
                    />
        </div>
    </div>
</template>

<script>
import InfographicItem from '../components/Infographic/InfographicItem'
import infographicsData from '../data.json'

export default {
    name: 'Infographics',
    components: {
        InfographicItem
    },
    data(){
        return {
           category: ''
        }
    },
    computed: {
        infographics: function() {
            let infographicsList = infographicsData.infographics;
            return infographicsList;
        },
        categories: function() {
            let categoriesList = infographicsData.categories;
            return categoriesList;
        },
        filterByCategory: function(){
            return this.infographics.filter(item => !item.category.indexOf(this.category))
        },
        getButtonClass: function() {
            let className = '';
            switch(this.category) {
                case 'vocabulary': 
                    className = 'red';
                    break;
                case 'grammar':
                    className = 'yellow';
                    break;
            }
            return className;
        }
    }
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
.colorSelect {
    background-color: bisque;
}
.red {
    background-color: red;
}

.yellow{
    background-color: yellow;
}
</style>
