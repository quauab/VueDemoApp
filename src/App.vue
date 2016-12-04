<template>
  <div id="app">
	<Test></Test>
  </div>
</template>

<script>
import Test from './components/test'

export default {
  name: 'app',
  components: {
    Test
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: rgb(20,80,150);
  background: rgb(240, 245, 255);
  margin-top: 60px;
  border-radius:10px;
  padding:1%;
  box-shadow:5px 5px 15px rgb(20,80,150);
}
</style>
