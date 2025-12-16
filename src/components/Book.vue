<script>
export default {
    data(){
        return{
            books: [
                {
                name: "Computer",
                price: 200,
                author: "ABC",
                tags: ["Programming"],
                },
                {
                name: "Physics",
                price: 250,
                author: "DEf",
                tags: ["Motions"],
                },
                {
                name: "Math",
                price: 220,
                author: "XYZ",
                tags: [],
                },
            ],
        }
    },
}
</script>

<template>
    <br><br>
    <h2>Example of For Loop called v-for in Vue</h2>
    <br>

    <div class="wrapper">
        <div class="card" v-for="(book, index) in books">
            <p>Book: {{ index + 1 }}</p>
            <h3>{{ book.name }}</h3>
            <p>{{ book.price }}</p>
            <p>{{ book.author }}</p>
        </div>
    </div>
    <br>
    <h4 v-for="num in 10">{{ num }}</h4>
</template>

<style scoped>
    .wrapper {
        display: flex;
        flex-wrap: 20px;
        gap: 20px;
    }
    .card {
        border: 2px solid black;
        background-color: lightblue;
        border-radius: 10px;
        margin-bottom: 20px;
        padding: 10px;
    }
</style>