<template>
  <MyComponent v-if="!login" data="Welcome App Vue" />
  <div v-else>
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import MyComponent from './components/MyComponent.vue'

export default {
  name: 'App',
  data() {
    return {
      login: false
    }
  },
  components: {
    HelloWorld,
    MyComponent
  },
  methods: {
    userAuth(userData) {
      console.log(userData.user, userData.email)
      //this.login = true
    }
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
