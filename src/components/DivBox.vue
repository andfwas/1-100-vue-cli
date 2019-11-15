<template>
  <div class="divbox">
    <h1>{{ msg }}</h1>
    <input v-model="multi" type="range" min="1" max="20">
    <Divs v-bind:mult="parseInt(multi)"></Divs>
  </div>
</template>

<script>
import Divs from './Divs.vue'
export default {
  name: 'DivBox',
  props: {
    msg: String,
    mult: Number
  },
  components: {
    Divs
  },
  data: function() {
    return {
      multi: 10
    }
  }
};
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
