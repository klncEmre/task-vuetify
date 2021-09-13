<template>
  <v-card
  elevation="20"
  outlined
  shaped
  >
    <v-form v-model="valid">
    <v-container>
      <v-col>
        <v-row
          cols="12"
          md="4"
        >
          <v-text-field
            v-model="Username" 
            label="Username"
            required
          ></v-text-field>
        </v-row>


        <v-row
          cols="12"
          md="4"
        >
          <v-text-field
            v-model="password"
            label="Password"
            required
          ></v-text-field>
        </v-row>

        <v-row
          cols="12"
          md="4"
        >
          <v-btn  @click="submit"> Login</v-btn>
          
        </v-row>

      </v-col>
    </v-container>
  </v-form>
  </v-card>
  
</template>
<script>


export default({
  
  data:() => ({
      valid: false,
      Username: '',
  
      password: '',
      
  }),
  methods: {
    submit () {
      if(this.Username === "emre.kilinc" && this.password == "admin123"){
          this.$router.push({name: 'About'})
      }
      
    
    }
  },
})
</script>

