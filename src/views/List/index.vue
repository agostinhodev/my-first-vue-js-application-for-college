<template>
  <div>
    
    <b-table 
      striped 
      hover
      :fields="fields"
      :items="items" 
      
      />
   
  </div>
  
</template>
<script>

  import { BTable } from "bootstrap-vue";

  export default{

    components:{

      BTable

    },

    data(){

      return{

        items: JSON.parse(localStorage.getItem('people')) , 

        fields:[

          {
            key: 'name', 
            label: 'Name:', 
            sortable: 'true'
          },
          {
            key: 'age', 
            label: 'Age:',
            sortable: true
          }

        ]

      }

    }

  }  

</script>