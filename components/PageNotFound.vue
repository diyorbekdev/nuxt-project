<template>
    <div>
        <h1>Page Not Found</h1>
        <img :src="require('@/assets/images/fe25.jpg')" alt="">
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
    div {
        display: flex;
        margin-top: -5%;
        align-items: center;
        justify-content: center;
    }
    h1 {
        font-size: 5rem;
        margin: 0 20px;
    }
    img {
        width: 10rem;
    }
</style>