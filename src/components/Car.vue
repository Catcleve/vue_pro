<template>
    <div>
        <h3>品牌：{{brand}}</h3>
        <h3>价格：{{price}}</h3>
        <h3>颜色：{{color}}</h3>
        <h3>解决方案的价格：{{cprice}}</h3>
        <button @click="addPrice">价格加一</button>
        <button @click="addCPrice">解决方案价格加一</button>
    </div>
</template>

<script>
export default {
    // data(){
    //     return {
    //         brand : "奔驰001",
    //         price : 20,
    //         color : "black"
    //     }
    // },
    props : {
        brand : {
            type : String,
            required : true
        },
        price : {
            type : Number,
            required : true
        },
        color : {
            type : String,
            default : "白色"
        }
    },
    data (){
        return{
            cprice : this.price
        }
    },
    /*
    vue.runtime.esm.js:4609 [Vue warn]: 
    Avoid mutating a prop directly since the value will be overwritten whenever 
    the parent component re-renders. Instead, use a data or computed property 
    based on the prop's value
    如果直接修改props中的值，会导致父级组件刷新时，修改过的值变成默认值
    解决方法:重新定义中转变量cprice
    */
    methods : {
        addPrice(){
            this.price++
        },
        addCPrice(){
            this.cprice++
        }
    }
}
</script>