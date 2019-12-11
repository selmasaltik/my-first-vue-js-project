<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1>{{ msg }}</h1>
    <hr>
    <UserList/>
    <Calculator/>
    <Dashboard/>
  </div>
</template>

<script>
import UserList from './components/UserList';
import Calculator from './components/Calculator';
import Dashboard from './components/Dashboard';
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to My Vue.js App'
    }
  },
  components : {
    'UserList' : UserList,
    'Calculator' : Calculator,
    'Dashboard' : Dashboard,
    }
  }
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 60px;
}

h1, h2 {
  font-weight: normal;
}

a {
  color: #42b983;
}
</style>
