<template>
  <div id="app">
    <div class="container">
      <quote-grid :quotes='quotes'></quote-grid>
    </div>
  </div>
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue'
export default {
 data(){
   return {
     quotes: [
       'First Quote',
       'second quotes'
     ]
   }
 },
 components:{
   'quote-grid' : QuoteGrid
 }
}
</script>

<style>

</style>
