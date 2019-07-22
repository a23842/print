<template>
 <div id="hello">
  <button @click="printDemo">测试打印</button>
    <vue-easy-print tableShow ref="easyPrint">
      <template slot-scope="func">
          <print :getChineseNumber="func.getChineseNumber" />
      </template>
    </vue-easy-print>
</div>
</template>

<script>
import vueEasyPrint from "vue-easy-print"
import print from "./print"
export default {
  name: "HelloWorld",
  data() {
    return {
    }
  },
  methods: {
    printDemo() {
      this.$refs.easyPrint.print();
    }
  },
  components: {
    vueEasyPrint,
    print
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
