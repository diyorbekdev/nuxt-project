<template>
  <div>
    <Header />
    <LargeCardDisplay v-for="cardInfo in largeCardInfo" :key="cardInfo.id" :cardInfo="cardInfo"/>
    <SmallCardDisplay v-for="cardInfo in smallCardInfo" :key="cardInfo.id" :cardInfo="cardInfo"/>
  </div>
</template>
<script>
import {largeCardSections, smallCardSections} from "@/assets/data.js"

export default {
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections,
    }
  },
}
</script>
