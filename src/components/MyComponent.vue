<template>
  <h1>
    {{data}}
  </h1>
</template>

<script>
export default {
  name: "MyComponent",
  props: ["data"],
  beforeMount() {
    console.log(this.data)
  }
}
</script>

<style scoped>
h1{
  color: #0022AA;
}
</style>