<script>
import Counter from "@/components/Counter.vue"
import Header from "@/components/Header.vue"
import Accordion from "@/components/Accordion.vue"
import Sentence from "@/components/Sentence.vue"

export default {
  components: {
    Counter,
    Header,
    Accordion,
    Sentence,
  },
}
</script>

<template>
  <Header />
  <Counter />
  <Accordion /> 
</template>


<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
</style>
