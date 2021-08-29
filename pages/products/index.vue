<template lang="">
    <div>
        <LargeCardDisplay :cardInfo="largeCardInfo[0]"/>
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
  }
}
</script>
<style lang="">
    
</style>