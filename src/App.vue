<template>
  <div id="app">
    <parent-component>
      <p>Ini adalah beberapa konten dari komponen induk yang dimasukkan melalui slot.</p>
    </parent-component>
  </div>
</template>

<script>
import ParentComponent from './components/ParentComponent.vue';

export default {
  name: 'App',
  components: {
    ParentComponent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #84aacf;
  margin-top: 60px;
  padding: 10px;
}
</style>
