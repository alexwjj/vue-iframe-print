<template>
  <div id="app">
    <h1>打印整页</h1>
    <button v-print>打印整页</button>

    <h1>局部打印</h1>
    <div id="printDiv1">
      且随疾风前行，身后亦需流心
    </div>

    <button v-print="'#printDiv1'">只打印指定 DOM（指令）</button>

    <div id="printDiv2">
      谎言并不伤人，真相才是快刀
    </div>

    <button v-print="printObj">只打印指定 DOM（对象）</button>
  </div>
</template>
<script>
export default {
  name: "app",
  data() {
    return {
      printObj: {
        id: "printDiv2",
        popTitle: "vue-iframe-print",
        extraCss: "https://www.baidu.com/,https://www.baidu.com/",
        extraHead: '<meta http-equiv="Content-Language"content="zh-cn"/>',
      },
    };
  },

  mounted() {},
};
</script>

<style>
#app {
  margin-top: 100px;
  text-align: center;
}
#printDiv1, #printDiv2{
	margin-top:20px;
}
</style>
