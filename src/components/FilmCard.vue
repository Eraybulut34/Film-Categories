<template>
  <div>
    <div class="film-card">
      <img :src="imageUrl" alt="img" class="film-card-image" :href="href" />
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class Filmcard extends Vue {
  @Prop() private imageUrl!: string;
  @Prop() private href!: string;
  @Prop() private routerLink!: string;
}
</script>

