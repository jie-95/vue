<template>
  <!-- 1 .number修饰符-把值parseFloat转数值再赋予给v-model对应的变量
         2 .trim修饰 - 去除首尾两边空格
         3 .lazy修饰符 - 失去焦点内容改变时(onchange事件), 把内容同步给v-model的变量 -->
  <div>
    <div>
      <span>年龄:</span>
      <input type="text" v-model.number="username" />
    </div>
    <div>
      <span>人生格言:</span>
      <input type="text" v-model.trim="txt" />
    </div>
    <div>
      <span>自我介绍:</span>
      <textarea v-model.lazy="pr"></textarea>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      username: "",
      txt: "",
      pr: "",
    }
  },
}
</script>
