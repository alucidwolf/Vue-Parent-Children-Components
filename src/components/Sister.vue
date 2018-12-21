<template>
  <div>
    <b-card :title="thecardtitle" footer-tag="footer">
      <p class="card-text">sister</p>
      <b-button variant="primary" @click="messageBrother">Message Brother</b-button>
      <div slot="footer" v-if="messagedaughter" v-html="messagedaughter"></div>
    </b-card>
  </div>
</template>

<script>
  export default {
    props: ["messagedaughter"],
    data() {
      return {
        thecardtitle: 'child'
      }
    },
    methods: {
      messageBrother() {
        this.$emit('sistersaid', 'mom said do hw')
      }
    }
  }

</script>

<style>

</style>
