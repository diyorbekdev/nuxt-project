<template lang="">
    <NuxtLink :to="`products/${cardsItem.id}`" class="card-container">
        <img class="image" :src="require(`@/assets/images/${cardsItem.image || 'fe1.jpg'}`)" alt="">
    </NuxtLink>
</template>
<script>
export default {
    props: ['cardsItem']
}
</script>
<style scoped>
    .card-container {
        width: 24%;
        height: 12.5rem;
        border-radius: 0.5rem;
        overflow: hidden;
        margin-bottom: 1.5rem;
        cursor: pointer;
    }
    .image {
        width: 100%;
        height: 100%
    }
</style>