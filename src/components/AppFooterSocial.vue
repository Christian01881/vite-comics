<template>
    <div id="FooterSocial">
        <div class="container h-100 d-flex justify-content-between align-items-center">
            <div>
                <div class="text-uppercase CPM-btn">Sign-up now</div>
            </div>
            <div class="d-flex align-items-center">
                <p class="text-uppercase text-primary w-50 fs-4 pt-2">follow us</p>
                <ul class="d-flex justify-content-between align-items-center w-100 gap-3">
                    <li class="color-dark" v-for="(link, index) in SocialLinks" :key="index"><a><img :src="getImagePath(`../assets/images/${link.img}`)" alt=""></a></li>
                </ul>
            </div>
        </div>  
    </div>
</template>

<script>
import { socialLinks } from '../data/data';
    export default {
        name: 'AppFooterSocial',
        data(){
            return{
                SocialLinks: socialLinks
            }   
        },
        methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        },
     }
    }

</script>

<style lang="scss" scoped>
   
   #FooterSocial{
        width: 100%;
        height: 80px;
        background-color: #303030;

        .w-50{
            width: 50px;
        }

        li{
            list-style: none;
            cursor: pointer;

            &:hover{
                scale: 1.3;
            }
        }
    }

    .CPM-btn{
        border: 4px solid #0183fc;
        padding: 6px 18px;
        color: white;
        cursor: pointer;
        font-size: 20px;
    }

</style>