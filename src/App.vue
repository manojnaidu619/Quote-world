<template>
  <div id="app">
    <div class="container">
      <add-quote :quotes='quotes'></add-quote>
      <quote-grid :quotes='quotes'></quote-grid>
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
 }
}
</script>

<style>

</style>
