<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <Default msg="Welcome to Your Vue.js App" class="text-light"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Default from '@/components/Default.vue'

export default {
  name: 'Home',
  components: {
    Default
  }
}
</script>
