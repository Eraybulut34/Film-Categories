<template>
  <div class="home">
    <CarouselSlider />
    <div class="container">
      <carousel
        class="categories"
        :dots="false"
        :responsive="{
          0: { items: 1, nav: false },
          900: { items: 2, nav: true },
          1200: { items: 4, nav: true },
        }"
      >
        <div v-for="category in categories" :key="category.name">
          <router-link :to="{ name: 'Film', params: { id: category.id } }">
            <FilmCard :newTitle="category.name" :imageUrl="category.img"
          /></router-link></div
      ></carousel>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import CarouselSlider from "@/components/CarouselSlider.vue";
import FilmCard from "@/components/FilmCard.vue";
import carousel from "vue-owl-carousel";

@Component({
  components: {
    CarouselSlider,
    FilmCard,
    carousel,
  },
  data() {
    return {
      categories: [
        {
          id: 1,
          name: "neighboor",
          img: "https://mediacms01.digiturkplay.com/sa_bc/PT0000346717/neighbor-the-2017_220x286.jpg",
        },
        {
          id: 2,
          name: "avatar",
          img: "https://img-s1.onedio.com/id-52d7c61f43516df04300005f/rev-0/w-600/h-897/f-jpg/s-fcf82db0d47f693fce19cdd4106a76aebf32225c.jpg",
        },
        {
          id: 3,
          name: "cin2",
          img: "https://mediacms01.digiturkplay.com/sa_bc/PT0000345053/cin-bebek2-2020_220x286.jpg",
        },
        {
          id: 4,
          name: "weneedtotalk",
          img: "https://mediacms01.digiturkplay.com/sa_bc/PT0000339332/we-need-to-talk-about-al-2020_220x286.jpg",
        },
        {
          id: 5,
          name: "croodlar",
          img: "https://mediacms01.digiturkplay.com/sa_bc/PT0000340899/croods-a-new-age-the_220x286.jpg",
        },
        {
          id: 6,
          name: "minari",
          img: "https://mediacms01.digiturkplay.com/sa_bc/PT0000325694/minari-turkce_220x286.jpg",
        },
      ],
    };
  },
})
export default class Home extends Vue {}
</script>
