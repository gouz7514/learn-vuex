<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div class="counter">
    {{counter}}
  </div>
  <div class="buttons">
    <button @click="increment">+</button>
    <button @click="decrement">-</button>
  </div>
</template>

<script>
import {mapState} from 'vuex'

export default {
  name: 'App',
  data() {
    return {
      // counter: 0
    }
  },
  methods: {
    increment() {
      console.log(this.counter)
      this.$store.commit('increment')
    },
    decrement() {
      this.$store.commit('decrement')
    }
  },
  computed: {
    ...mapState(['counter'])
    // counter() {
    //   // return this.$store.state.counter
      
    // }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
