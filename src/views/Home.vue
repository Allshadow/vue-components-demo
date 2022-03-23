<template>
  <div class="home">
    <!-- <el-button type="primary" @click="toCount">点击加count</el-button>
    <el-button>{{count}}</el-button> -->
    <base-print></base-print>
  </div>
</template>

<script>
  import BasePrint from '@/components/BasePrint'
  import {mapState} from 'vuex'
export default {
  name: 'Home',
  components: {
    BasePrint
  },
  created() {

  },
  computed:{
    // count: this.$store.state.count
    // count(){
    //   return this.$store.state.count
    // }

    ...mapState(['count'])
  },
  methods:{
    toCount(){
      this.$store.commit('changCount', 5)
    }
  }
}
</script>
