<script>
export default {
    data(){
        return{
            error: {
                name: null,
                email: null,
                password: null,
            },
        }
    },
    methods:{
        validateForm(){
            this.error.name = "Name is required."
            this.error.email = "Email is required."
            this.error.password = "Password is required."
        },
    },
}
</script>

<template>
    <br><br>
    <h2>Form</h2>
    <form action="">
        <div>
            <label for="">Name</label>
            <input type="text" />
            <div v-show="error.name">{{ error.name }}</div>
        </div>

        <div>
            <label for="">Email</label>
            <input type="text" />
            <div v-show="error.email">{{ error.email }}</div>
        </div>

        <div>
            <label for="">Password</label>
            <input type="text" />
            <div v-show="error.password">{{ error.password }}</div>
        </div>

        <button type="button" @click="validateForm">Submit</button>
    </form>
    <br><br>
</template>

<style scoped>
    
</style>