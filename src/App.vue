<template>
  <v-ons-navigator 
  :page-stack="pageStack"
  @push-page="pushPage"
  :options="getOptions()"
  >
    
  </v-ons-navigator>
</template>

<script>
import Page1 from './pages/Page1.vue'

  export default{
   data(){
    return{
       pageStack : [Page1]
    }
   },

   methods : {
    pushPage(page){
      this.pageStack.push(page)
    },
    getOptions(){
      return {
        animation : 'fade'
      }
    }
   }
  }

</script>

<style>
  
</style>
