<template>
  <MultiSlider :num="numInputs" :min="0" :max="100" @input="handleSliderInput" />
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js Appa"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import MultiSlider from './components/MultiSlider.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    MultiSlider
  },
  data() {
    return {
      numInputs: 8,
      inputs: []
    }
  },
  methods: {
    handleSliderInput(e) {
      this.inputs = e
      console.log(e)
    }
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
