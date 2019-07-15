<template>
 <div class="row">
   <div class="col-4" v-for="(quote,index) in quotes">
     <div class="card">
       <div class="card-body" @click="remove(index)">
         {{quote}}
       </div>
     </div>
   </div>
 </div>
</template>

<script>
 export default{
   props: ['quotes'],
   methods: {
     remove(index){
       this.$emit('removeQuote',index)
       console.log(`QuoteGrid : ${index}`)
     }
   }
 }
</script>

<style scoped>
 .card-body{
   font-family: 'Pacifico', cursive;
   font-size: 20px;
   text-align: center;
   cursor: pointer;
  }
  .card{
    border: 2px dashed DarkGrey;
    margin: 5px;
  }
  .card:hover{
    background-color: #efc2ca;
  }
</style>
