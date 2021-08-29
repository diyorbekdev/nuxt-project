<template lang="">
    <div class="container">
        <h1 class="header">{{ cardInfo.title }}</h1>
        <p class="snippet">{{ cardInfo.snippet }}</p>
        <div class="cards-container">
            <LargeCard v-for="card in cardInfo.cards" :key="card.id" :LargeCard="card"/>
        </div>
    </div>
</template>
<script>


export default {
    data() {
        return {
        }
    },
    props: ['cardInfo']
}
</script>
<style scoped>
    .container {
    margin-top: 2rem;
}
    .header {
        font-weight: 700;
        font-size: 1.5rem;
    }
    .snippet {
        color: grey;
        margin-bottom: 1.5rem;
    }
    .cards-container {
        display: flex;
        justify-content: space-between;
    }
</style>