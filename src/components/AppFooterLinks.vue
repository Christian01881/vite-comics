<template>
    <div id="FooterTop">
        <div class="container d-flex justify-content-between">
            <div class="d-flex">
                <div>
                    <ul  v-for="(items, index) in FooterLinks" :key="index" v-show="index < 2">
                    <li class="title"><h3>{{ items.title }}</h3></li>
                    <li v-for="(link, index) in items.links" :key="index"><a>{{ link.text }}</a></li>
                    </ul> 
                </div>
                <div class="d-flex">
                    <ul class="px-4" v-for="(items, index) in FooterLinks" :key="index" v-show="index >= 2">
                    <li class="title"><h3>{{ items.title }}</h3></li>
                    <li v-for="(link, index) in items.links" :key="index"><a>{{ link.text }}</a></li>
                    </ul> 
                </div>
            </div>
            <div>
                <img src="../assets/images/dc-logo-bg.png" alt="">
            </div>
        </div>
    </div>
</template>

<script>
import { footerLinks } from '../data/data';

    export default {
        name: 'AppFooterLinks',
        data(){
            return{
                FooterLinks: footerLinks
            }
        },
    }
</script>

<style lang="scss" scoped>

    #FooterTop{
        height: 350px;
        background-image: url(../assets/images/footer-bg.jpg);
        background-size: cover;
        margin: 0;
        overflow: hidden;

        img{
            position: relative;
            top: -100px;
        }
    }

    ul{
        margin-top: 20px;
        padding: 0;
    }

    li{
        font-size: 13px;
        color: #668787;
        list-style: none;

        h3{
            color: white;
        }

        a{
            cursor: pointer;
        }

        &:hover{
                text-decoration: underline;
            }
    }

    .title{
        font-size: 25px;
    }
</style>