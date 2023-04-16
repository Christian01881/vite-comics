<template>
    <div class="bg-dark">
        <div class=" contentContainer">
            <div class="current text-uppercase text-white fs-4 d-flex align-items-center justify-content-center">
            current series
            </div>
         </div>    
    </div>
    <div class="bg-dark">
        <div class="d-flex flex-wrap container">
            <AppCard v-for="comic in comics" :image="comic.thumb" :title="comic.series" />
        </div>
    </div>
    <div class="d-flex align-items-center justify-content-center bg-dark pb-4">
        <div class="mybutton text-uppercase text-white fs-4 d-flex align-items-center justify-content-center">
            load more
        </div>
    </div>
</template>

<script>
import { comicsData } from '../data/data';
import AppCard from './AppCard.vue';
    export default {
        name: 'AppContent',
        components : {
        AppCard,
        },
        data(){
            return{
                comics: comicsData
            }
        }
    }

</script>

<style lang="scss" scoped>
    .contentContainer{
        height: 500px;
        background-image: url(../assets/images/jumbotron.jpg);
        background-size: cover;
    }

    .current{
        position: relative;
        bottom: -470px;
        left: 120px;
        height: 50px;
        width:200px;
        background-color: #0d6efd;
        cursor: pointer;
    }

    .mybutton{
        background-color: #0d6efd;
        height: 50px;
        width: 200px;
        cursor: pointer;
    }
</style>