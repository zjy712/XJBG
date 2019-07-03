<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <One></One>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import One from '@/views/one.vue'

export default {
  name: 'home',
  components: {
    HelloWorld,
    One
  }
}
</script>
