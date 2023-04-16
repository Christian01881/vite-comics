<template>
    <div id="header">
        <div class="container h-100 d-flex justify-content-between align-items-center">
            <div>
                <img src="../assets/images/dc-logo.png" alt="">
            </div>
            <div class="h-100 d-flex align-items-center">
                <ul class="d-flex gap-4 align-items-center text-uppercase h-100">
                    <li v-for="(link, index) in navLinks" :key="index" class="d-flex align-items-center"><a>{{ link.text }}</a></li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
import {links} from '../data/data.js';
    export default {
        name: 'AppHeader',
        data(){
            return{
                navLinks: links,
            }
        },
    }
</script>

<style lang="scss" scoped>
    #header{
        height: 120px;
        width: 100%;
        background-color: white;
        position: fixed;
        z-index: 1000;

        img{
            display: block;
            width: 80px;
            height: 80px;
        }

        ul{
            margin: 0,
        }

        li{
            font-size: 20px;
            list-style: none;
            height: 100%;
            cursor: pointer;
            border-bottom: 5px solid transparent;
            &:hover{
                color: #0282f9;
                border-bottom: 5px solid #0282f9 ;
            }
        }

        .active{
            color: #0282f9;
            border-bottom: 5px solid #0282f9 ;
        }
    }
</style>