<template>
    <div class="bg-primary">
        <div class="container d-flex align-items-center gap-5 HMain">
            <ul class="d-flex justify-content-between align-items-center w-100 ps-5 pe-5">
                <li class="color-dark" v-for="(link, index) in mainLinks" :key="index"><a><img :src="getImagePath(`../assets/images/${link.src}`)" :alt="`${link.alt}`"><span>{{ link.description }}</span></a></li>
            </ul>
        </div>
    </div>
</template>

<script>
import { mainContent } from '../data/data.js';
    export default {
        name: 'AppMain',
        data(){
            return{
                mainLinks: mainContent
            }
        },
        methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
    }
</script>

<style lang="scss" scoped>
    .HMain{
        height: 180px;

        img{
            width: 55px;
            height: 56px;
        }

        li{
            list-style: none;
        }
        
        a{
            text-decoration: none;
            cursor: pointer;
            span{
                color: white;
                margin-left: 10px;
                font-size: 20px;
            }
        }
    }
</style>