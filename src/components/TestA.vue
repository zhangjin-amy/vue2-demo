<template>
  <div>
    <p @click="onClick">TestA: {{ msg }}</p>
  </div>
</template>

<script>
// import TestChild from './TestChild.vue';
export default {
  name: 'TestA',
  props: {
    msg: Number,
  },
  methods: {
    onClick() {
      console.log('---onClick TestA');
      this.$emit("update", 2)
    }
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
