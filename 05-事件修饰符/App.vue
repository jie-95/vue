<templa<template>
  <div @click="fatherFn">
    <!--vue对事件进行了修饰符设置, 在事件后面.修饰符名即可使用更多的功能
        .prevent - 阻止默认行为
        .once - 程序运行期间, 只触发一次事件处理函数-->
    <button @click.stop='btn'>.stop阻止事件冒泡</button>
    <a href="http://www.baidu.com">.prevent阻止默认行为</a>
    <button @click.once='btn1'>.once程序运行期间, 只触发一次事件处理函数</button>
  </div>
</template>

<script>
export default {
  methods: {
    fatherFn(){
      console.log('冒泡了');
    },
    btn(){
      console.log('.stop');
    },
    btn1(){
      console.log('.once');
    }
  }
}
</script>

<style>
</style>
