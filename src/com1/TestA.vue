<template>
  <div>
    <p @click="onClickA">TestA:</p>
  </div>
</template>

<script>

export default {
  name: 'TestA',
  inject:['onChangeMsg'],
  methods: {
    onClickA() {
      console.log('onClickA');
      // this.$emit('onChangeMsg', 'hi');
      this.onChangeMsg(2);
    }
  },
  mounted() {
    console.log('------mounted', this.onChangeMsg);
  }
}
</script>

<style>
</style>
