<template>
  <div id="app">
    <!-- <HelloWorld/>
    <Class/>
    <Conditional/>
    <For/>
    <Event/>
    <Input/> -->
    <Product/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Class from './components/Class'
import Conditional from './components/Conditional'
import For from './components/For'
import Event from './components/Event'
import Input from './components/Input'
import Product from './components/Props/Product'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Class,
    Conditional,
    For,
    Event,
    Input,
    Product
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
