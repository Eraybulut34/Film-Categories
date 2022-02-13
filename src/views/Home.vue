<template>
  <div class="home">
    <HelloWorld/>
    <div class="container">
<carousel></carousel>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import HelloWorld from '@/components/HelloWorld.vue';
import CategoryCard from '@/components/CategoryCard.vue';
import carousel from 'vue-owl-carousel';

@Component({
  components: {
    HelloWorld,
    CategoryCard,
    carousel
  },
  
})
export default class Home extends Vue {
getData():void{
this.$axios.get('https://gateway.marvel.com/v1/public/comics?ts=100&apikey=9ba68562b5c70ba6442264f6c5add1c2&hash=cdf3beb7b14c2e38b26b3f2fdef6a2ee').then(response => {
  console.log(response.data.data);
});
}
beforeMount():void{
  this.getData();
}
}
</script>
