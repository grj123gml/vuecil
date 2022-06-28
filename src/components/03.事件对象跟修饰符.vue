<!-- 1. 事件触发, 无传值, 可以直接获取事件对象
    2. 事件触发, 传值, 需要手动传入$event -->
<template>
  <div>
    <a @click="one" href="http://www.baidu.com">阻止百度</a>
    <hr>
    <a @click="two(10, $event)" href="http://www.baidu.com">阻止去百度</a>

    <hr>
     <div @click="fatherFn">
    <!-- vue对事件进行了修饰符设置, 在事件后面.修饰符名即可使用更多的功能 -->
    <button @click.stop="btn">.stop阻止事件冒泡</button>
    <br>
    <a href="http://www.baidu.com" @click.prevent.stop="btn">.prevent阻止默认行为</a> <br>
    <button @click.once="btn">.once程序运行期间, 只触发一次事件处理函数</button>
  </div>
  </div>
</template>

<script>
export default {
  methods: {
    // 1. 事件触发, 无传值, 可以直接获取事件对象
    one(e){
      e.preventDefault()
    },
    // 2. 事件触发, 传值, 需要手动传入$event
    two(num, e){
      e.preventDefault()
    },
     fatherFn(){
      console.log("father被触发");
    },
    btn(){
      console.log(1);
    }
  }
}
</script>