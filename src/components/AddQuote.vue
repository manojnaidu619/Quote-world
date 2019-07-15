<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="col-6">
        <form>
          <div class="form-group">
            <textarea class="form-control" placeholder="Add a Quote" rows="3" v-model='newQuote'></textarea><br>
            <button type="button" class="btn btn-success btn-large" @click.prevent="PushQuote()" name="button">Add Quote</button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
 export default{
     props: ['quotes'],
     data(){
       return {
         newQuote: ""
       }
     },
     methods:{
       PushQuote(){
         if(this.newQuote.length > 3 && this.newQuote.length < 100 && this.quotes.length < 10){
           this.quotes.push(this.newQuote)
           this.newQuote = ""
         }
       }
     }
 }
</script>

<style>
 .container{
   margin-top: 50px;
 }
 .row{
   margin-top: 20px;
 }
</style>
