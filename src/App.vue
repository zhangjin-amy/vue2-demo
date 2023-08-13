<template>
  <div id="app">
    <!-- <p>in app msg:{{ msg }}</p>
    <p>in app count:{{ count }}</p> -->
    <!-- <TestIndex :msg="msg" @update="update" name="jinjin"/> -->
    <!-- <TestIndex /> -->
    <!-- <TestIndex v-model="msg" /> -->
    <!-- <TestIndex v-model="count" /> -->
    <TestIndex />
  </div>
</template>

<script>
// import TestIndex from './components/TestIndex.vue'
// import TestIndex from './com1/TestIndex.vue'
// import TestIndex from './com2/TestIndex.vue'
// import TestIndex from './com3/TestIndex.vue'
import TestIndex from './com4/TestIndex.vue'

export default {
  name: 'App',
  components: {
    TestIndex
  },
  provide() {
    return {
      onChangeMsg: this.onChangeMsg,
    }
  },
  data() {
    return {
      msg: 1,
      count: 0
    }
  },
  // watch: {
  //   'count': function(newVal, val) {
  //     console.log('------count watch', newVal, val);
  //   }
  // },
  methods: {
    // update() {
    //   this.msg = 'amy'
    // }
    // update(val) {
    //   console.log('----app update');
    //   this.msg = val;
    // },
    onChangeMsg(val) {
      console.log('****onChangeMsg');
      this.msg = val;
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
