<template>
    <h1>{{heading}}</h1>

    <div class="counter">
        <button @click="decrement" class="btn">Decrease</button>
        <h2 :class="{'active-heading': isActive}">{{ count }}</h2>
        <button @click="increment"  class="btn">Increase</button>
    </div>
</template>

<script>
    export default{
        data(){
            return{
                count: 0,
                isActive: true
            }
        },
        methods:{
            increment(){
                this.count++
                if(this.count>0){
                    this.isActive = false
                }
            },
            decrement(){
                this.count--
                if(this.count<0){
                    this.isActive = true
                }
            },
        }
    }
</script>

<style>
    h1{
        margin: 20px 0;
        text-align: center;
    }
    .counter{
        display: flex;
        justify-content: center;
        gap: 30px;
    }
    .btn{
        color: blue;
    }
    .active-heading{
        color: red;
    }
</style>