<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>Guia Clientes</h1>
    <div v-for="(cliente, index) in clientes" :key="cliente.id">
      <h1>{{ index }}</h1>
      <Cliente :cliente="cliente" />
    </div>
  </div>
</template>

<script> 
import Cliente from './components/Cliente'

export default {
  name: 'App',
  data(){
    return{
      clientes: [
        {
          id: 1,
          nome: 'João',
          numero: '123456789',
          email: 'joao@gmail.com'
        }, {
          id: 2,
          nome: 'Maria',
          numero: '987654321',
          email: 'maria@gmail.com'
        }, {
          id: 3,
          nome: 'Pedro',
          numero: '123456789',
          email: 'pedro@gmail.com'
        }, {
          id: 4,
          nome: 'Ana',
          numero: '987654321',
          email: 'ana@gmail.com'
        }, {
          id: 5,
          nome: 'José',
          numero: '123456789',
          email: 'josé@gmail.com'
        }
      ]
    }
  },
  components: {
    Cliente
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
