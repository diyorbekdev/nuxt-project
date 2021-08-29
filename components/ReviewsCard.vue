<template lang="">
    <div>
        <div v-if="reviews.results">
            <Reviews v-for="reviewer in reviews.results" :key='reviewer.dob.age' :reviewProps="reviewer"/>
        </div>
        <div v-else>
            Loading...
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            reviews: []
        }
    },
    async fetch() {
        this.reviews = await fetch('https://randomuser.me/api/?result=5').then((res) => res.json())
    }
}
</script>
<style lang="">
    
</style>