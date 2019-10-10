<template>
  <v-app>
    <Navbar/>
    <v-content>
      <h1>Hola mundo</h1>

    </v-content>
    <Footer/>
  </v-app>
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'home',
  components: {
    Navbar,
    Footer
  }
}
</script>
