<template>
  <div class="base-pdf">
    <el-button type="primary" @click="toPrint">点击打印PDF</el-button>
  </div>
</template>

<script>
// 引入 pdf 
import printJS from 'print-js'

export default {
  data(){
    return {
      publicPath: process.env.BASE_URL
    }
  },
  methods:{
    toPrint(){
      printJS('http://zy-zymreal-source-test.oss-cn-shanghai.aliyuncs.com/8f60a8fdaa889ac8dc8571bd4d0d507e82c169de.pdf')
    }
  }
}
</script>

<style>

</style>