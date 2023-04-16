<template>
    <div class="bg-dark d-flex justify-content-center align-items-center comic-card mt-5">
        <div class="d-flex flex-column">
            <img :src="image" :alt="title">
            <div class="text-cover text-center text-sm-start">
            <p class="text-white text-uppercase mt-3 ">{{ title }}</p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'AppCard',
        props: ['image', 'title'],
    }
</script>

<style lang="scss" scoped>
    
    img{
        width: 200px;
        height: 200px;
    }

    .comic-card{
        width: calc(100% / 6);
        cursor: pointer;

        &:hover p{
            color: #0d6efd !important;
        }
    }

    p{
        max-width: 200px;
        height: 50px;
    }
</style>