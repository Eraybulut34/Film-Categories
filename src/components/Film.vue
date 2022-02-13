<template>
  <div>
    <div class="film">
      <div class="film-card">
        <div class="film-image">
          <img :src="img" alt="img" class="film-card-image" />
        </div>
        <div class="info">
          <div class="film-title">
            <h3>{{ name }}</h3>
          </div>
          <div class="info-inner">
            <div class="category">Film Türü: {{ category }}</div>
            <div class="film-duration">Süre: {{ duration }} Dk.</div>
            <div class="film-year">Yıl: {{ year }}</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component({
  data() {
    return {
      id: this.$route.params.id,
      name: null,
      img: null,
      category: null,
      duration: null,
      year: null,
    };
  },
})
export default class Film extends Vue {
  getData(): void {
    this.$axios
      .get("https://6209611f6df46f0017f4c4d9.mockapi.io/film/" + this.$data.id)
      .then((response) => {
        const data = response.data;
        this.$data.img = data.img;
        this.$data.name = data.name;
        this.$data.category = data.category;
        this.$data.duration = data.duration;
        this.$data.year = data.year;
      });
  }
  beforeMount() {
    this.getData();
  }
}
</script>

