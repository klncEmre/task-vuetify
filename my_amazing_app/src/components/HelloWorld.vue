<template>
  <v-form v-model="valid">
    <v-container>
      <v-row>
        <v-col
          cols="12"
          md="4"
        >
          <v-text-field
            v-model="Username" 
            label="Username"
            required
          ></v-text-field>
        </v-col>


        <v-col
          cols="12"
          md="4"
        >
          <v-text-field
            v-model="password"
            label="Password"
            required
          ></v-text-field>
        </v-col>

        <v-col
          cols="12"
          md="4"
        >
          <v-btn  @click="submit"> Login</v-btn>
          
        </v-col>

      </v-row>
    </v-container>
  </v-form>
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

