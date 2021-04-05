<template>
<div class="full-width" sticky="true">
    <b-container>
        <b-navbar toggleable="lg">
            <b-navbar-brand href="#">
                <router-link to="/">
                Learn Danish
                </router-link>
            </b-navbar-brand>

            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

            <b-collapse id="nav-collapse" is-nav>
            <!-- Right aligned nav items -->
                <b-navbar-nav class="ml-auto">
                    <b-nav-form>
                        <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
                    </b-nav-form>
                <b-nav-item-dropdown text="Categories" right class="button_categories">
                    <b-dropdown-item v-for="item in categories" :key="item.id">
                        <b-badge variant="primary">
                            <router-link
                            :to="{
                                name: 'Infographics',
                                params: { category: item.category}
                            }"
                            >
                                {{item.category}}
                            </router-link>
                        </b-badge>
                    </b-dropdown-item>
                </b-nav-item-dropdown>
            </b-navbar-nav>
            </b-collapse>
        </b-navbar>
    </b-container>
</div>
</template>

<script>
import categoriesData from '../../data.json'
export default {
  name: 'TopMenu',
  data() {
    return {
      categories: categoriesData.infographics
    };
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.full-width {
    width: 100%;
    background-color: white;
    box-shadow: 0 2px 4px -1px rgba(0, 0, 0, 0.5);
}
.button_categories {
    background-color: #F53855;
    border: none;
    border-radius: 5px;
}

</style>
