<template>
    <div class="pyq">
        <div class="Circle" >
            <div class="tou" @click="abo('NavigAtion')">{{msg.tou}}</div>
            <div class="title">{{msg.title}}</div>
            <slot name="slo"></slot>
        </div>
        
    </div>
</template>

<script>
    export default {
        name:"FaXian",
        data() {
            return {
                key:''
            }
        },
        props:{
            msg:{
                type:Object,
                default:()=>{
                    return {
                        tou:" ",
                        title:"我是默认值"
                    }
                }
            },
            
            
        },
        watch:{
           
        },
        methods: {
            abo(str){
                this.$router.push(str)
            }
        },
    }
</script>

<style  scoped>
    .pyq{
        width: 400px;
        height: 70px;
        
    }
    .Circle{
        width: 400px;
        height: 50px;
        display: flex;
        flex-direction: row;
        justify-content: flex-start;
        align-items: center;
        background: cornflowerblue;

    }
    .tou{
        width: 30px;
        height: 30px;
        background: chartreuse;
        margin-left: 20px
    }
    .title{
        margin-left: 20px
    }
    
</style>