<template>
  <div>
    <b-card :title="thecardtitle" footer-tag="footer">
      <p class="card-text">brother</p>
      <b-button variant="primary" @click="messageSister">Message Sister</b-button>
      <div slot="footer" v-if="messageson" v-html="messageson"></div>
    </b-card>
  </div>
</template>

<script>
  export default {
    props: ['messageson'],
    data() {
      return {
        thecardtitle: 'child'
      }
    },
    methods:{
      messageSister(){
        this.$emit('brothersaid', 'mom said to hw')
      }
    }
  }

</script>

<style>

</style>
