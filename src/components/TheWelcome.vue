<template>
  <div id="app">
    <input v-model="num1">
    <input v-model="num2">
    <button @click="calculate('+')">+</button>
    <button @click="calculate('-')">-</button>
    <button @click="calculate('*')">*</button>
    <button @click="calculate('/')">/</button>
    <button @click="clear">Clear</button>
    <p>Hasil: {{ result }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num1: 0,
      num2: 0,
      result: null
    }
  },
  methods: {
    calculate(operation) {
      if(operation == '+') this.result = parseFloat(this.num1) + parseFloat(this.num2)
      if(operation == '-') this.result = parseFloat(this.num1) - parseFloat(this.num2)
      if(operation == '*') this.result = parseFloat(this.num1) * parseFloat(this.num2)
      if(operation == '/') this.result = parseFloat(this.num1) / parseFloat(this.num2)
    },
    clear() {
      this.num1 = 0
      this.num2 = 0
      this.result = null
    }
  }
}
</script>

<style scoped>
#app {
  text-align: center;
  color: #2c3e50;
}
</style>
