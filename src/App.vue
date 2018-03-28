<template>
  <div id="app">
    <HelloWorld/>
    <Form/>
    <MainTable/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Form from './components/Form'
import MainTable from './components/MainTable'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Form,
    MainTable
  }
}
</script>

<style lang="scss">
//variables:
$main-h1-color:rgb(74, 57, 172);

//main css

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.vdp-datepicker{
    input{
        font-size: 14px;
        text-align: center;
        width: 100%;
        padding: 4px 0;
    }
}
</style>
