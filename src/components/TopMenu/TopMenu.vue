<template>
<div class="full-width" sticky="true">
    <b-container>
        <b-navbar toggleable="lg">
            <b-navbar-brand href="#">Learn Danish</b-navbar-brand>

            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

            <b-collapse id="nav-collapse" is-nav>
            <!-- Right aligned nav items -->
                <b-navbar-nav class="ml-auto">
                    <b-nav-form>
                        <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
                    </b-nav-form>
                    <b-nav-item href="#">
                        <router-link to="/about"><i class="fa fa-fw fa-star-o"></i>About</router-link>
                    </b-nav-item>
                <b-nav-item-dropdown text="Categories" right class="button_categories">
                    <b-dropdown-item>
                        <router-link to="/about">
                        <b-badge variant="primary">Grammar</b-badge>
                        </router-link>
                    </b-dropdown-item>
                    <b-dropdown-item href="#">
                        <router-link to="/infographics">
                            <b-badge variant="success">Everyday language</b-badge>
                        </router-link>
                    </b-dropdown-item>
                    <b-dropdown-item href="#">
                        <b-badge variant="warning">Danish video</b-badge>
                    </b-dropdown-item>
                </b-nav-item-dropdown>
            </b-navbar-nav>
            </b-collapse>
        </b-navbar>
    </b-container>
</div>
</template>

<script>
export default {
  name: 'TopMenu',
  props: {
    msg: String
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
