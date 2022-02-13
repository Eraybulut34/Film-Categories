<template>
  <div id="app">
    <div id="nav">
<Navbar/>
    </div>
    <router-view/>
    <Footer/>
  </div>
</template>

.<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Navbar from '@/components/Navbar.vue'
import Footer from '@/components/Footer.vue'

export default Vue.extend({
  components:{
    Navbar,
    Footer
  
  }
})
</script>

<style lang="scss">
</style>
