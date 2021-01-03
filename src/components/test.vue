<template>
    <div>
        我是First页面的组件显示
        {{msg}}
        {{abc}}
        <!-- <slot></slot> -->
        <slot name="a"></slot>
        <button @click="test">点我</button>
        
    </div>
</template>

<script>
    export default {
        name:"Test",
        props:{//是一个属性
            msg:{//里面的内容是固定得写法，type，和default
                type:String,
                default:"我是默认值"
            },
             msgs:{//里面的内容是固定得写法，type，和default
                type:Object,
                default:()=>{//当type是object的时候，default一定是一个函数，需要有返回值return[]数组也可以
                    return{

                    }
                }
            }
        },
        data() {
            return {
                key:""
            }
        },
        watch:{
            key:function (newValue,oldValue) {
                console.log("key"+newValue)
                console.log("keykey"+oldValue)

            }
        },
        computed:{//计算属性
            abc:function () {//属性下一定是function，有返回值
            // return this.msg=123是不能改变的
             this.key=this.msg
            // this.sss=111;//可以将父页面的msg重新赋值，再改变新的值
            return this.msg + 1111
            }
        },
        methods: {
            test(){
                console.log("点击了按钮")
                this.$emit("test",12322)
            }
        },
    }
</script>

<style  scoped>

</style>