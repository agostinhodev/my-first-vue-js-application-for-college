<template>
  <div>
    
    <b-container>

      <b-row class="justify-content-md-center mt-4">

        <b-col col md="8">

          <b-card 
            header="You need to register to become a member of our team 🤣🤣🤣"
            header-bg-variant="primary"
            header-text-variant="white"
          >
          
          <b-card-text>
            <b-form @submit="handleSubmit">

              <b-form-group 
                description="What's your name?"
                label="Name: 🤔">

                <b-form-input
                v-model="name"
                required
                >
                </b-form-input>

              </b-form-group>

              <b-form-group 
                description="Age:"
                label="How old are you? 😱">

                <b-form-input
                v-model="age"
                required
                type="number"
                min=1
                >
                </b-form-input>

              </b-form-group>

              <b-form-group>

                <b-button
                
                type="submit"
                variant="outline-primary"

                >

                  😎 Submit

                </b-button>

              </b-form-group>

            </b-form>
          </b-card-text>
          
          </b-card>

        </b-col>

      </b-row>

    </b-container>
   
  </div>
  
</template>
<script>

  export default{

    data(){

      return{

        name: '',
        age: ''

      }

    },
    methods: {

      handleSubmit(event){

        event.preventDefault();
        
        let person = {

          name: this.name,
          age: this.age

        };

        this.$emit('pushItem', person);

        alert('Record was created')
        this.name = '';
        this.age = '';
        

      }

    }

  }
 
</script>