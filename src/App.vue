<template>
  <div id="app">
    <div class="container">
      <add-quote :quotes='quotes'></add-quote>
      <quote-grid :quotes='quotes' @removeQuote="deleteQuote"></quote-grid>
      <div class="row justify-content-center">
        <div class="col-5 alert alert-primary">
           info : Click on the Quote to delete it!
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue'
import AddQuote from './components/AddQuote.vue'
export default {
 data(){
   return {
     quotes: [
       'This is a Default Quote'
     ]
   }
 },
 components:{
   'quote-grid' : QuoteGrid,
   'add-quote' : AddQuote
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
