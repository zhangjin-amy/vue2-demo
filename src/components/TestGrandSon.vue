<template>
  <div class="hello">
    <!-- <p>TestGrandSon：{{ msg }}</p> -->
    <TestA v-bind="$attrs" v-on="$listeners" />
  </div>
</template>

<script>
import TestA from './TestA.vue';
export default {
  name: 'TestGrandSon',
  // props: {
  //   msg: String
  // },
  components: {
    TestA
  }
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
