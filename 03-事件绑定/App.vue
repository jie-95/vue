<template>
  <div>
    <p>你要购买商品的数量: {{ count }}</p>
    <!-- 1. 绑定事件
     语法: v-on:事件名="少量代码"
     语法: v-on:事件名="methods里函数名"
     语法: v-on:事件名="methods里函数名(值)"
     语法: @事件名="methods里函数名"
     -->
    <button @click="count++">+1</button>
    <button v-on:click="btn">+1</button>
    <button v-on:click="btn1(5)">+5</button>
    <button @click="count--">减少1</button>
  </div>
</template>

<script>
export default {
  data () {
    return {
      count: 1,
    }
  },
  methods: {
    btn () {
      console.log(this)
      this.count++
    },
    btn1 (val) {
      this.count += val
    },
  },
}
</script>

<style></style>
