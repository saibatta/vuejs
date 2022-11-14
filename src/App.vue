<template>
  <TextBinding msg="app to text binding"/>
</template>

<script>
import TextBinding from './components/TextBinding.vue'

export default {
  name: 'App',
  components: {
    TextBinding
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
