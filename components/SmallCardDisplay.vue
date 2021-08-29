<template lang="">
    <div class="container">
        <h1 class="header">{{ cardInfo.title }}</h1>
        <div class="card-container">
            <SmallCard v-for="card in cardInfo.cards" :key="card.id" :cardsItem="card"/>
        </div>
    </div>
</template>
<script>
export default {
    props: ['cardInfo']
}
</script>
<style scoped>
    .container {
        padding: 2rem 0
    }
    .header {
        font-weight: 700;
        font-size: 1.5rem;
        margin-bottom: 2rem;
    }
    .card-container {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
    }
</style>