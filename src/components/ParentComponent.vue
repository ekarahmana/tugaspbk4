<template>
    <div class="parent">
      <h1>Parent Component</h1>
      <child-component @data-emitted="handleDataEmitted"></child-component>
      <p>Data Dari Child: {{ childData }}</p>
      <slot></slot> <!-- Slot untuk menyisipkan konten dari komponen induk -->
    </div>
  </template>
  
  <script>
  import { ref } from 'vue';
  import ChildComponent from './ChildComponent.vue';
  
  export default {
    name: 'ParentComponent',
    components: {
      ChildComponent
    },
    setup() {
      const childData = ref('');
  
      function handleDataEmitted(data) {
        childData.value = data;
        alert(data); // Alert menampilkan data yang diterima dari ChildComponent
      }
  
      return {
        childData,
        handleDataEmitted
      };
    }
  }
  </script>
  
  <style scoped>
  .parent {
    padding: 20px;
    border: 2px solid #333;
    border-radius: 15px;
    margin: 10px;
    background-color: #451515;
    color: antiquewhite;
  }
  </style>
  