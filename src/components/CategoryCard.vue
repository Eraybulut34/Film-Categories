<template>
      <div>
    <div class="category-card">
      <div>
        <img :src="imageUrl" alt="img" />
        <div class="category-card-text">
          {{ newTitle }}
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class HelloWorld extends Vue {
 
 @Prop() private newTitle!: string;
  


}
</script>

