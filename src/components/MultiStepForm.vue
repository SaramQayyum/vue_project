<script>
export default {
    data(){
        return{
            step: 1
        }
    },
    methods:{
        handleNextButton(){
            if(this.step < 3){
                this.step++
            }
        },
        handleBackButton(){
            if(this.step > 1){
                this.step--
            }
        },
    },
}
</script>

<template>
    <h2>Multi Step Form</h2>
    <form action="">
        <div v-show="step === 1">
            <label for="">Name</label>
            <input type="text" />
        </div>

        <div v-show="step === 2">
            <label for="">Email</label>
            <input type="text" />
        </div>

        <div v-show="step === 3">
            <label for="">Password</label>
            <input type="text" />
        </div>

        <button type="button" @click="handleBackButton" v-show="step > 1"> Back </button>
        <button type="button" @click="handleNextButton"> {{ step <= 2 ? "Next" : "Submit" }} </button>
    </form>
</template>

<style scoped>

</style>