<template>
  <div class="container">
    <div v-bind:key="block.id" v-for="block in blocks" class="well">
      <template v-if="block.id === 123">
        <p>Text only content block</p>
        <button v-on:click="updateControlPanel">Turn cp1 to true</button>
      </template>
      <template v-if="block.id === 321">
        <p>Media left content block</p>
      </template>
      <template v-if="block.id === 456">
        <p>Media right content block</p>
      </template>
    </div>
  </div>

</template>

<script>
  export default {
    name: 'ContentBlock',
    data() {
      return {
        blocks: [{
            id: 123,
            text: '1',
          },
          {
            id: 321,
            text: '2',
          },
          {
            id: 456,
            text: '3',
          }
        ]
      }
    },
    mounted() {
      this.$root.$on('eventing', data => {
        console.log(data);
      })
    }
  }

</script>

<style>

</style>
