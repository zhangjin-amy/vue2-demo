<template>
  <div>
    <p>TestIndex</p>
    <TestA />
  </div>
</template>

<script>
import TestA from './TestA.vue';
export default {
  name: 'TestDemo',
  // props: ['msg'],
  // inject: ['msg'],
  components: {
    TestA,
  },
  data() {
    return {
    }
  },
  methods: {
  }
}
</script>

<style>
</style>
