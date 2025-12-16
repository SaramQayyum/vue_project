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

    <h1 v-show="vShowState">Hello</h1>
    <br>
    <br>

    <h1 v-if="awesome == 'awesome'">Vue is Awesome</h1>
    <h1 v-else-if="awesome == 'superb'">Vue is Superb</h1>
    <h1 v-else>Vue is a Javascript Framework</h1>

    <button @click="toggle('awesome')">Toggle to Awesome</button>
    <button @click="toggle('superb')">Toggle to Superb</button>
    <button @click="toggle('')">Toggle to None</button>
</template>

<script>
    export default{
        data(){
            return{
                isVisible: false,
                awesome: "suberb",
                vShowState: false,
            }
        },
        methods:{
            toggleVisible(){
                this.isVisible = !this.isVisible
            },
            toggle(value){
                this.awesome = value
            }
        }
    }
</script>

<style scoped>
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