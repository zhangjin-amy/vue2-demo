<template>
  <div>
    <p @click="onClick">TestIndex {{ count }}</p>
  </div>
</template>

<script>

export default {
  name: 'TestIndex',
  model: {
    // 👹👹👹是props不是prop
    prop: 'count',
    event: 'update'
  },
  props: {
    count: {
      type: Number
    }
  },
  methods: {
    onClick() {
      console.log('-----onClick');
      this.$emit('update', 666);
    }
  }
}
</script>

<style>
</style>
