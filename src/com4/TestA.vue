<template>
  <div>
    <p @click="onClick">TestA: {{ value }}</p>
    <TestA1 v-model="count" ref="testa1"/>
  </div>
</template>

<script>
import TestA1 from './TestA1.vue';
export default {
  name: 'TestA',
  props: ['value'],
  components: {
    TestA1,
  },
  data() {
    return {
      count: this.value
    }
  },
  watch: {
    'value': function(newVal) {
      this.count = newVal
    }
  },
  methods: {
    onClick() {
      console.log('---onClick', this.$refs.testa1);
      this.$emit('input', this.value + 1)

    }
  }
}
</script>

<style>
</style>
