<template>
  <div class="home">
    
    <v-main>
      <v-container fluid>
        <div class="d-flex justify-center mt-10">
          <v-img src="@/assets/images/icon.png" style="max-width: 12rem"></v-img> 
          
        </div>
        <div class="d-flex justify-center">
         <h1>Sam C. Parker</h1>
          
        </div>
        <div class="d-flex justify-center mt-3 mb-15">
         <p><a href="#">about me</a> | <a href="#">projects</a> | <a href="#">blog</a> | <a href="https://www.github.com/samcparker" target="_blank">github</a></p>
          
        </div>

  <hr class="mb-15" style="color: rgb(0, 0, 0)">
  <v-row>
    <v-col xs="12" sm="12" md="12" lg="6" xl="6"><showcase></showcase></v-col>

    <v-col xs="12" sm="12" md="12" lg="6" xl="6"><blog></blog></v-col>
      


  </v-row>

      </v-container>

      
    </v-main>
  </div>
</template>

<script>
// @ is an alias to /src
import NavBar from '@/components/NavBar.vue'
import Showcase from '@/components/Showcase.vue'
import Blog from '@/components/Blog.vue'

export default {
  name: 'Home',
  components: {
    NavBar, Showcase, Blog
  }
}
</script>

<style scoped>
body {
  background-color: #D1D4A9;
}

a {
  color: black;
}

h1 {
  font-family: 'Playfair Display', serif;
  font-size: 3rem;
}
</style>
