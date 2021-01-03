<template>
    <div class="navig">
        <navigation >
            <div class="navi" slot="nav">
                <div class="imgs" @click="fanhui">
            <img src="../assets/xy.png" alt="">
            </div>
            </div>
        </navigation>
        
        <div class="">sdfsdfdscsdf</div>
    </div>
</template>

<script>
import NavigOne from '@/components/NavigOne.vue';
    export default {
        comments:{
            NavigOne
            
            },
            data() {
                return {
                    
                }
            },
            methods: {
                fanhui(){
                    this.$router.go(-1)
                }
            },
    }
</script>

<style scoped>
    .navig{
        width: 400px;
        height: 500px;
        background: cornflowerblue;
    }
    .navi{
        width: 400px;
        height: 40px;
        background: cornsilk;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
    }
    .imgs{

    }
</style>