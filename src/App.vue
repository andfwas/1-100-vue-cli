<template>
  <div id="app">
    <DivBox msg="DivBox"/>
  </div>
</template>

<script>
import DivBox from './components/DivBox.vue';

export default {
  name: 'app',
  components: {
    DivBox
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
