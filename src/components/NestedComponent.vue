<template>
    <div class="nested">
      <h3>Nested Component</h3>
      <ChildComponent @data-emitted="handleData"/>
    </div>
  </template>
  
  <script>
  import ChildComponent from './ChildComponent.vue';
  
  export default {
    name: 'NestedComponent',
    components: {
      ChildComponent
    },
    methods: {
      handleData(data) {
        this.$emit('data-emitted', data);
      }
    }
  }
  </script>
  
  <style scoped>
  .nested {
    padding: 10px;
    border: 1px solid #000;
    margin: 10px;
  }
  </style>
  