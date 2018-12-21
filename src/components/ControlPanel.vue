<template>
  <aside>
    <h1>Control Panel</h1>
    <div>{{title}} is <b>{{open}}</b></div>
  </aside>
</template>

<script>
  export default {
    name: 'ControlPanel',
    data() {
      return {
        title: 'panel1',
        open: false
      }
    }
  }

</script>

<style>

</style>
