<template>
  <div id="app">
    
    <h1>Vue Memory Game</h1>

    <board></board>

    <button v-on:click="resetBoard">New Game</button>

  </div>
</template>

<script>
import board from './components/board.vue';

export default {
  name: 'app',

  components: {
    board
  },

  data() {
    return {
    }
  },

  methods: {
    resetBoard: function() {
      location.reload();
    }
  }
}
</script>

<style lang="scss">

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 40px;
}

h1, h2 {
  font-weight: normal;
  margin: 24px auto;
}

button {
  background-color: LightSeaGreen;
  border: none;
  border-radius: 2px;
  color: white;
  font-weight: bold;
  font-size: 14px;
  margin-bottom: 24px;
  padding: 8px 12px;
}

button:hover {
  background-color: #30a39c;
  cursor: pointer;
}

</style>
