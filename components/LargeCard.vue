<template lang="">
    <div class="card">
        <img class="image" :src="require(`@/assets/images/${LargeCard.image || 'fe1.jpg'}`)" alt="">
        <h3 class="header">{{ LargeCard.title }}</h3>
        <p class="snippet">
            {{LargeCard.snippet }}
        </p>
    </div>
</template>
<script>
export default {
    props: ['LargeCard']
}
</script>
<style scoped>
    .card {
        width: 31.5%;
        height: 25rem;
        border: none;
        overflow: hidden;
        padding: 0;
        cursor: pointer;
    }
    .image {
        height: 65%;
        border-radius: 0.5rem;
    }
    .header {
        font-size: 1.15rem;
        margin-top: 0.4rem;
    }
    .snippet {
        color: grey
    }
</style>