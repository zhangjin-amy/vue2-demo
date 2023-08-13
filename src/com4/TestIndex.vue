<template>
  <div>
    TestIndex: {{ count }}
    <TestA v-model="count" ref="testA"/>
    <button @click="onClickBtn">TestIndex Btn</button>
  </div>
</template>

<script>
import TestA from './TestA.vue';
export default {
  name: 'TestIndex',
  data() {
    return {
      count: 0
    }
  },
  components: {
    TestA
  },
  methods: {
    onClickBtn() {
      // 获取子组件的值
      console.log('------onClickBtn', this.$refs.testA.$refs.testa1.value);
      // console.log('------onClickBtn', this.$refs.testa1);
    }
  },
  
}
</script>

<style>
</style>
