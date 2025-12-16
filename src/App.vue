<script>
import Counter from "@/components/Counter.vue"
import Header from "@/components/Header.vue"
import Accordion from "@/components/Accordion.vue"
import Sentence from "@/components/Sentence.vue"
import Form from "@/components/Form.vue"
import MultiStepForm from "@/components/MultiStepForm.vue"
import Book from "@/components/Book.vue"

export default {
  components: {
    Counter,
    Header,
    Accordion,
    Sentence,
    Form,
    MultiStepForm,
    Book,
  },
  // data(){
  //   return {
  //     showHeader: true,
  //   }
  // }
}
</script>

<template>
  <!-- <Header v-if="showHeader" /> -->
  <Header />
  <Counter />
  <Accordion /> 
  <Form />
  <MultiStepForm />
  <Book />
</template>


<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
</style>
