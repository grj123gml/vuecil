<template>
  <div>
    <input type="text" v-bind:value='val' @input="Fn">
  </div>
</template>

<script>
export default {
data(){
  return{
    val:""
  }
},
methods:{
  Fn(e){
  this.val=e.target.value
  }
}
}
</script>

<style>

</style>
