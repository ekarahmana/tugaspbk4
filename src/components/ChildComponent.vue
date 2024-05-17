<template>
  <div class="child">
    <button @click="sendData">Kirim Data to Parent</button>
  </div>
</template>

<script>
export default {
  name: 'ChildComponent',
  methods: {
    sendData() {
      this.$emit('data-emitted', 'Hello everyone saya rahma');
    }
  }
}
</script>

<style scoped>
.child {
  padding: 10px;
  border: 1px solid #ccc;
  margin: 10px;
  background: #a84646;
  border-radius: 10px;
}
button {
  color:bisque
}
</style>
