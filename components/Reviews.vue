<template>
    <div>
        <h3>Customer Reviews</h3>
        <!-- {{$fetchState}} -->
        <div v-if="!$fetchState.pending">
            <!-- {{reviewers}} -->
            <ReviewCard 
            v-for="reviewer in reviewers.results"
            :key="reviewer.login.uuid"
            :review="reviewer"/>

        </div>
        <div v-else>
            Data Not Found
        </div>
    </div>
</template>

<script>
    export default {
        data(){
            return {
                reviewers: null
            }
        },
        async fetch(){
            this.reviewers = await fetch(
                'https://randomuser.me/api/?results=5'
            ).then(res=>res.json())
        }
    }
</script>

<style scoped>

</style>