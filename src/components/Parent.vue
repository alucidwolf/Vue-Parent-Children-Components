<template>
  <div class="container">
    <b-card-group deck>
      <b-card :title="thecardtitle">
        <p class="card-text">
          card text
        </p>
        <b-button variant="warning" @click="momSaidChill" v-if="stopFighting()">stop fighting</b-button>
      </b-card>
      <brother :messageson="messageson" @brothersaid="messageDaughter($event)"></brother>
      <sister :messagedaughter="messagedaughter" @sistersaid="messageSon($event)"></sister>
    </b-card-group>
  </div>
</template>

<script>
import Brother from './Brother.vue';
import Sister from './Sister.vue';

  export default {
    components: {
      Brother,
      Sister
    },
    data() {
      return {
        thecardtitle: 'Parent!',
        messagedaughter: '',
        messageson: ''
      }
    },
    methods: {
      messageDaughter(message) {
        this.messagedaughter = message;
      },
      messageSon(message) {
        this.messageson = message;
      },
      stopFighting(){
        if(this.messagedaughter && this.messageson){
          return true;
        }
        return false;
      },
      momSaidChill(){
        this.messagedaughter = '';
        this.messageson = '';
      }
    }
  }

</script>

<style>

</style>
