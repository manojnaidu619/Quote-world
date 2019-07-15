<template>
  <div class="row">
    <div class="col">
      <h3>Quotes Added</h3>
      <div class="progress">
        <div class="progress-bar" role="progressbar" :style="{width: (count * 10) +'%'}" aria-valuenow="25" aria-valuemin="0" aria-valuemax="10">{{count}}/10</div>
      </div>
    </div>
  </div>
</template>

<script>
 export default{
   props: ['count']
 }
</script>

<style scoped>
 .progress{
   height:35px;
 }
 .progress-bar{
    background-color: Coral;
    font-weight: bold;
    font-size: 20px;
 }
</style>
