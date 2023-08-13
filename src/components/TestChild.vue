<template>
  <div class="hello">
    <!-- <h1 @click="onClick">TestChild: {{ msg }}</h1> -->
    <TestGrandSon 
      v-bind="$attrs" 
      v-on="$listeners" 
    />
  </div>
</template>

<script>
import TestGrandSon from './TestGrandSon.vue';
export default {
  name: 'TestChild',
  // props: {
  //   msg: String,
  // },
  components: {
    TestGrandSon
  }
  // methods: {
  //   onClick() {
  //     console.log('TestChild onClik');
  //     this.$emit('update', 'amy');
  //   }
  // }
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
