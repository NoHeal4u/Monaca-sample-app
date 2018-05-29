<template>
    <v-ons-page 
    @init="onInit"
    @show="onShow"
    @hide="onHide"
    @destroy="onDestroy"
    >
    <v-ons-toolbar>
      <div class="left">
        Levi
      </div>
      <div class="center">
        Centar
      </div>
      <div class="right">
        Desni
      </div>
    </v-ons-toolbar>
      <div class="content">
        <v-ons-search-input placeholder="Bla...." v-model="title"/>
        <v-ons-button modifier="large" @click="onClick">Do not click me</v-ons-button>
      </div>
    </v-ons-page>
</template>
<script>
import Page2 from './Page2.vue'

  export default{
    data() {
      return {
        title: 'My app'
      };
    },
    methods: {
      alert() {
        this.$ons.notification.alert('This is an Onsen UI alert notification test.');
      },
      onInit(event) {
        console.log('INIT')
      },
       onShow() {
        console.log('Show')
      },
       onHide() {
        console.log('Hide')
      },
       onDestroy() {
        console.log('Destroy')
      },
      onClick(){
        this.$emit('push-page', {

          extends : Page2,
          onsNavigatorProps:{
            name:'Tom'
          }
        })
      },
    }
  };
</script>
