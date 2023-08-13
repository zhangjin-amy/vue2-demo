<template>
  <div>
    <!-- <TestA v-model="msg" /> -->
    <p @click="onClick">TestIndex: {{ value }}</p>
  </div>
</template>

<script>
// import TestA from './TestA.vue';
export default {
  name: 'TestIndex',
  props: {
    value: {
      type: Number
    }
  },
  data() {
    return {
      myMsg: ''
    }
  },
  methods: {
    onClick() {
      console.log('----onClick');
      // ok
      this.$emit('input', 2);
    }
  },
  mounted() {
    console.log('-----mounted', this);
  }
  // components: {
  //   TestA
  // }
}
</script>

<style>
</style>
