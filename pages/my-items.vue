<template>
    <div class="container">
        <NuxtLink to="/">Go Back</NuxtLink>
        <MyItems v-for="item in myRentals" :key="item.id" :item="item"/>
    </div>
</template>

<script>
import {mapState} from 'vuex'

    export default {
        computed: {
        ...mapState(["myRentals"])
    }
    }
</script>

<style scoped>
    .container {
        padding: 5rem 0
    }
</style>