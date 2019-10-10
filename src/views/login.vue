<template>    
  <v-app>
    <Navbar/>
    <v-content class="fill-height" fluid>
      <v-card width="35%" class="mx-auto mt-5 center">
        <v-card-title>
          <h1 class= "display-1">Login</h1>
        </v-card-title>
        <v-card-text>
          <v-form>
            <v-text-field 
              label="Username" 
              prepend-icon ="mdi-account-circle"
            />
            <v-text-field 
              :type= " showPassword ? 'text' : 'password'" 
              label="Password"
              prepend-icon = "mdi-lock"
              :append-icon = "showPassword ? 'mdi-eye' : 'mdi-eye-off'"
              @click:append="showPassword= !showPassword"
              />
          </v-form>
        </v-card-text>
        <v-divider></v-divider>
        <v-card-actions>
          <v-btn color = "success">Login</v-btn>
          <v-spacer></v-spacer>
          <v-btn color = "info">Register</v-btn>  
        </v-card-actions>
      </v-card>
    </v-content>
    <Footer/>
  </v-app>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import Footer from '@/components/Footer.vue'
export default {
  
  name: 'login',
  components: {
    Navbar,
    Footer
  },
  data: () =>({
      showPassword: false,
      links: [
          'Home',
          'Login',
          'Register'
      ]
  })
}
</script>