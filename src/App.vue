<template>
  <ConditionalStatements msg="Conditional Statement demo" />
</template>

<script>
import ConditionalStatements from './components/conditional.vue'

export default {
  name: 'App',
  components: {
    ConditionalStatements
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
}
</style>
