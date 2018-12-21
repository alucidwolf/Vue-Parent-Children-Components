<template>
  <div id="app">
    <HelloWorld msg="CMS Content"/>
    <Parent/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Parent from './components/Parent.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    Parent
  }
}
</script>

<style>
</style>
