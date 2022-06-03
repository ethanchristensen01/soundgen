<template>
  <div class="hello">
    <input v-for="i in num" type="range" :min="min" :max="max" ref="inputs" :key="i" @input.stop="handleInput"/>
  </div>
</template>

<script>
export default {
  name: 'MultiSlider',
  props: {
    num: Number,
    min: Number,
    max: Number,
  },
  methods: {
    handleInput() {
      this.$emit('input', this.$refs.inputs.map(input => input.value))
    }
  }
}
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
