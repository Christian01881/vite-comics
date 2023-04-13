<template>
    <div class="bg-dark">
        <div class="container contentContainer d-flex align-items-center">
            <h3 class="text-white">{{ text }}</h3>
         </div>
    </div>
</template>

<script>
    export default {
        name: 'AppContent',
        data(){
            return{
                text: '--->Content goes here<---'
            }
        }
    }
</script>

<style lang="scss" scoped>
    .contentContainer{
        height: 120px;
    }
</style>