<template>
<!--   <b-navbar
    toggleable="md"
    type="dark"
    variant="info">
    <b-navbar-brand :to="{ name: 'Home' }">Learn Danish</b-navbar-brand>
    <b-navbar-nav>
      <b-nav-item :to="{ name: 'Home' }">Home</b-nav-item>
      <b-nav-item :to="{ name: 'About' }">About</b-nav-item>
    </b-navbar-nav>
  </b-navbar> -->
   <div>
    <b-button v-b-toggle.sidebar-1>Toggle Sidebar</b-button>
    <b-sidebar id="sidebar-1" title="Sidebar" shadow>
      <div class="px-3 py-2">
        <p>
          Cras mattis consectetur purus sit amet fermentum. Cras justo odio, dapibus ac facilisis
          in, egestas eget quam. Morbi leo risus, porta ac consectetur ac, vestibulum at eros.
        </p>
        <b-img src="https://picsum.photos/500/500/?image=54" fluid thumbnail></b-img>
      </div>
    </b-sidebar>
  </div>
</template>
<script>
export default {
  name: 'Navbar'
};
</script>