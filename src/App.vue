<template>
  <div>
    <b-container class="text-center">
      <h2>My first Vue.js App 😁</h2>
      <h4>This is a simple Vue.JS application that i build for class exercise</h4>
    </b-container>
    

    <div>
    <b-tabs content-class="mt-3">
      <b-tab title="List of People" active>
        
        <list />

      </b-tab>
      <b-tab title="Register">
        
          <register />

      </b-tab>
    </b-tabs>
  </div>
    
  

  </div>
</template>

<script>
import { List, Register } from "@/views";

export default {
  name: "App",
  
  components: {
    'list':List,
    'register':Register,

  },
};
</script>

<style></style>
