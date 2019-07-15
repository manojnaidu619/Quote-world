<template>
 <div class="row">
   <div class="col-3" v-for="quote in quotes">
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

<style>

</style>
