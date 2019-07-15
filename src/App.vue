<template>
  <div id="app">
    <div class="container">
      <quote-progress :count="quotes.length"></quote-progress>
      <add-quote :quotes='quotes'></add-quote>
      <quote-grid :quotes='quotes' @removeQuote="deleteQuote"></quote-grid>
      <div v-if="this.quotes.length > 0" class="row justify-content-center">
        <div class="col alert alert-warning">
           info : Click on the Quote to delete it!
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue'
import AddQuote from './components/AddQuote.vue'
import ProgressBar from './components/ProgressBar.vue'
export default {
 data(){
   return {
     quotes: [
       'This is a Default Quote'
     ],
   }
 },
 components:{
   'quote-grid' : QuoteGrid,
   'add-quote' : AddQuote,
   'quote-progress' : ProgressBar
 },
 methods:{
   deleteQuote(index){
     this.quotes.splice(index, 1)
   }
 }
}
</script>

<style scoped>
 .alert{
   text-align:center;
   margin-top:30px;
 }
</style>
