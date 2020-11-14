<template>
  <div>
    <b-container class="text-center">
      <h2>My first Vue.js App 😁</h2>
      <h4>This is a simple Vue.JS application that i build for class exercise</h4>
    </b-container>
    

    <div>
    <b-tabs content-class="mt-3">
      <b-tab title="List of People" active>
        
        <list :listdata="items"/>

      </b-tab>
      <b-tab title="Register">
        
          <register @pushItem="getPushItem"/>

      </b-tab>
    </b-tabs>
  </div>
    
  

  </div>
</template>

<script>
import { List, Register } from "@/views";

export default {

  data: () =>{

    return {

      items: [

        {

          'name': 'Agostinho Celestino Barbosa Neto', 
          'age': 22

        },{

          'name': 'Arthur Martins Prates', 
          'age': 21

        },{

          'name': 'Marlon Áquila Cardoso Menegatti', 
          'age': 20

        }

      ]

    }

  },

  name: "App",
  
  components: {
    'list':List,
    'register':Register,

  },

  methods: {

    getPushItem( value ){

      this.items.push(value)

    }

  }
};
</script>

<style></style>
