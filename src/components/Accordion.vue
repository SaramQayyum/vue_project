<template>
    <div class="accordion">
        <header>
            <h3>Title</h3>
            <button @click="toggleVisible">{{ isVisible ? "-" : "+" }}</button>
        </header>
        <p class="content" :class="{'show-content': isVisible}">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit.
            Laborum ad delectus doloremque placeat esse quae atque eius aliquid dolorum, dolore,
            voluptates reiciendis a, suscipit nulla quibusdam voluptatibus omnis voluptas. Dignissimos.
        </p>
    </div>
</template>

<script>
    export default{
        data(){
            return{
                isVisible: false,
            }
        },
        methods:{
            toggleVisible(){
                this.isVisible = !this.isVisible
            }
        }
    }
</script>

<style>
    .accordion{
        max-width: 500px;
        border-radius: 10px;
        border: 2px solid royalblue;
        background-color: skyblue;
        overflow: hidden;
        margin: 40px 0px;
    }

    .accordion > header{
        background-color: darkblue;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 10px;
    }

    .accordion > header h3{
        color: white;
        margin: 0;
    }

    .accordion > header button{
        color: white;
        background-color: royalblue;
        font-size: 20px;
        border: 2px solid white;
        border-radius: 5px;
        width: 60px;
    }

    .accordion .content{
        display: none;
    }

    .accordion .show-content{
        display: block;
    }
</style>