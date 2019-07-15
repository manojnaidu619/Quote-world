<template>
 <div class="row">
   <div class="col-4" v-for="quote in quotes">
     <div class="card">
       <div class="card-body">
         {{quote}}
       </div>
     </div>
   </div>
 </div>
</template>

<script>
 export default{
   props: ['quotes']
 }
</script>

<style scoped>
 .card-body{
   font-family: 'Pacifico', cursive;
   font-size: 25px;
  }
</style>
