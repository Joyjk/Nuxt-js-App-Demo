<template>
  <div>
   
    <div class="container">
      <LargeCardDisplay
        v-for="largeCard in largeCardSections"
        :key="largeCard.id"
        :cardsSection="largeCard"
      />
      <SmallCardDisplay
      v-for="smallCard in smallCardSections"
      :key="smallCard.id"
      :cardSection="smallCard"
    />
    </div>
  </div>
</template>

<script>
import { smallCardSections, largeCardSections } from "@/assets/data.js";


export default {
  //components: { SmallCardDisplay },
  data() {
    return {
      largeCardSections,
      smallCardSections,
    };
  },
};
</script>

<style  scoped>
</style>