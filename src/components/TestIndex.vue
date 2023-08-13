<template>
  <div class="hello">
    <p @click="onClick">my name is {{ name }}, my msg is {{ msg }}</p>
    <!-- <TestFather v-bind="$attrs" v-on="$listeners" /> -->
    <TestFather :msg="msg" v-on="$listeners" />
  </div>
</template>

<script>
import TestFather from './TestFather.vue';
export default {
  name: 'TestIndex',
  props: {
    name: String,
    msg: Number,
  },
  components: {
    TestFather
  },
  methods: {
    onClick() {
      console.log('------TestIndex onClick');
      this.$emit('update', 7);
    },
  },
  // mounted() {
  //   console.log('----TestIndex mounted', this.$props);
  // },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
