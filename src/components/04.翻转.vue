<template>
  <div>
    <h1>{{message}}</h1>
    <button @click="btn">翻转文字</button>
  </div>
</template>

<script>
export default {
data(){
  return{
    message:"Hello,Vue"
  }
},
methods:{
  btn(){
    this.message=this.message.split('').reverse().join("")
  }
}
}
</script>

<style>

</style>
