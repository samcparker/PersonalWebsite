<template>
  <div id="app">
    <nav-bar class="nav-height"></nav-bar>
    <div class="nav-height" id="home"></div>
    <header>
      <hero></hero>
    </header>
    <main class="container container-fluid shadow-lg px-5 pb-5">
      <content-pane id="about" title="About Me" text="My name is Sam and I study computer science at the University of Kent. Lorem ipsum dolor sit, amet consectetur adipisicing elit. Praesentium, minus est. Commodi quisquam at amet eius? Adipisci fuga aliquid iure laborum porro perspiciatis temporibus, officia tenetur quidem sapiente repellendus. Explicabo?Lorem ipsum dolor sit, amet consectetur adipisicing elit. Praesentium, minus est. Commodi quisquam at amet eius? Adipisci fuga aliquid iure laborum porro perspiciatis temporibus, officia tenetur quidem sapiente repellendus. Explicabo?"></content-pane>

      <projects-pane id="projects"></projects-pane>
 
      <technical-skills-pane id="technical"></technical-skills-pane>
  
      <contact-pane id="contact"></contact-pane>
    </main>
    <footer class="jumbotron jumbotron-fluid mb-0 mt-5 pb-4">
      <div class="container">
<p class="lead mb-3">Thank you for visiting my website. It was made using Vue.js & Bootstrap 4.</p>
      <p><a href="https://github.com/juicehub/PortfolioWebsite" target="_blank">Check out the source on Github!</a></p>
      <p class="text-center mt-5">Sam C. Parker</p>
      </div>
      
    </footer>
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import ContentPane from './components/ContentPane.vue'
import ProjectsPane from './components/ProjectsPane.vue'
import TechnicalSkillsPane from './components/TechnicalSkillsPane.vue'
import ContactPane from './components/ContactPane.vue'
import Hero from './components/Hero.vue'

export default {
  name: 'App',
  components: {
    NavBar, ContentPane, ProjectsPane, TechnicalSkillsPane, ContactPane, Hero
  }
}
</script>

<style>
html {
            scroll-behavior: smooth
        }
section:before {
    height: 4rem;
    content: "";
    display:block;
}
.nav-height {
  height: 4rem;
}
h1 {
  text-decoration: none;
  border-bottom: 3px solid black;
  width: 100%;
}
main {
  background-color: white;
}
body {
  
  background-image: url("./assets/images/swirl.jpg");
}
</style>
