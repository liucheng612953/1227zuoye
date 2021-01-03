<template>
    <div>
        <!-- 我是First页面
        <Test v-bind:msg="key" v-on:test="test">我是slot插槽的显示</Test>
        <div slot="a">我是slot name="a"插槽的显示</div> -->
        <div>
        <faxian v-for="(m,index) in array" :key="index" v-bind:msg="m">
            <div slot="slo"></div>
        </faxian>
        </div>
        <LieBiao v-bind:msg="arr"></LieBiao>
    </div>
</template>

<script>
// import Test from '@/components/test.vue'
   import Faxian from '@/components/faxian.vue';
   import LieBiao from '@/components/liebiao.vue';
    export default {
        components:{
            //Test,
            Faxian,
            LieBiao
        },
        data() {
            return {
                key:"0",
                array:[
                    {
                        tou:" ",
                        title:"朋友圈"
                    },
                     {
                        tou:" ",
                        title:"视频号"
                    },
                     {
                        tou:" ",
                        title:"扫一扫"
                    },
                     {
                        tou:" ",
                        title:"摇一摇"
                    },
                     {
                        tou:" ",
                        title:"看一看"
                    },
                ],
                 arr:[
                    {
                      title:"零售",
                      content:"我是内容",
                      img:"我是图片"
                    },
                    {
                      title:"民生",
                      content:"我是内容",
                      img:"我是图片"
                    },
                    {
                      title:"政务",
                      content:"我是内容",
                      img:"我是图片"
                    },
                    {
                      title:"出行",
                      content:"我是内容",
                      img:"我是图片"
                    },
                    {
                      title:"医疗",
                      content:"我是内容",
                      img:"我是图片"
                    },
                ]
            }
        },
        methods: {
            // test(v){
            //     console.log("我是父布局的this.$emit"+" "+v)
            // }
        },
    }
</script>

<style  scoped>

</style>