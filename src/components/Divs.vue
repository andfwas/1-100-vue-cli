<template>
  <div>
    <button @click="getColor"></button>
    <div v-for="n in mult" :key="n">
      <div class="row">
        <div class="box" v-for="n in mult"  :key="n.toString()">{{n}}</div>

      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Divs',
  props: {
    mult: Number
  },
  methods: {
    getColor: function(e) {
      e.preventDefault()
      var r = Math.floor(Math.random() * 128)
      var g = Math.floor(Math.random() * 128)
      var b = Math.floor(Math.random() * 128)
      console.log(r)
      var color = "rgb(" + r + ", " + g + ", " + b + ");"
      var css = "background-color: " + color
      console.log(css)
      return css
    }
  }
};
</script>

<style scoped>
  .row {
    display: flex;
    flex-flow: row;
    width: 95%;
    margin: auto;
    padding: 0 0 0 0;
    margin: 0 0 0 0;
  }
  .box {
    width: 4.5vw;
    outline: none;
    height: 4.5vw;
  }
</style>