<template>
  <div id="app">
    <HelloWorld/>
    <Class/>
    <Conditional/>
    <For/>
    <Event/>
    <Input/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Class from './components/Class'
import Conditional from './components/Conditional'
import For from './components/For'
import Event from './components/Event'
import Input from './components/Input'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Class,
    Conditional,
    For,
    Event,
    Input
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  height: 100vh;
}

</style>
