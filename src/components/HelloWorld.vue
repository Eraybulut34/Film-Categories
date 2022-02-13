<template>
  <div class="carousel">
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      indicators
      img-width="500"
      img-height="200"
      style="text-shadow: 1px 1px 2px #333"
      @sliding-start="true"
      @sliding-end="false"
    >
      <b-carousel-slide
        caption="First slide"
        text="G.B.E.D. is a platform for the students to get the best of their knowledge and skills in the field of engineering."
        img-src="https://i.pinimg.com/originals/d4/dc/f5/d4dcf57454f20774d388057edd3ee526.jpg"
      ></b-carousel-slide>
      <b-carousel-slide img-src="https://c4.wallpaperflare.com/wallpaper/536/846/466/interstellar-movie-movies-wallpaper-preview.jpg">
        <h1>INTERSTELLAR</h1>
      </b-carousel-slide>
      <b-carousel-slide
        img-src="https://resimdiyari.com/_data/i/upload/2012/10/19/20121019130859-0f6e7275-me.jpg"
      ></b-carousel-slide>
    </b-carousel>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class HelloWorld extends Vue {
 
 @Prop() private msg!: string;
  


}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
