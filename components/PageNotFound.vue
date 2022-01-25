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
        align-items: center;
        justify-content: center;
        width: 30rem
    }
    h1 {
        font-size: 3.5rem;
    }
    img {
        width: 8rem;
        margin: 0 auto
    }
</style>