<template>
  <h1> {{data}} </h1>
  <form v-on:submit.prevent="onHandleSubmit($event)">
    <input type="text" placeholder="user" v-model="user">
    <input type="text" placeholder="email" v-model="email">
    <button>Enviar</button>
  </form>
</template>

<script>
export default {
  name: "MyComponent",
  props: ["data"],
  data() {
    return {
      user: "",
      email: ""
    }
  },
  beforeMount() {
    console.log(this.data)
  },
  methods: {
    onHandleSubmit(event) {
      console.log(event.target)
      const userData = {
        user: this.user,
        email: this.email
      }
      console.log(userData)
      console.log("sending")
      //this.$emit("userAuth", userData)
    }
  }
}
</script>

<style scoped>
h1{
  color: #0022AA;
}
</style>