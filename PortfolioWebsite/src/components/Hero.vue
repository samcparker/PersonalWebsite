<template>
  <div class="jumbotron jumbotron-fluid py-5" id="hero-image">"
        <div class="container py-5">
          <h2 class="display-3" style="color: white">Sam C. Parker</h2>
          <p class="lead" style="color: white"><em>Welcome to my website. I hope you enjoy your stay.</em></p>
        </div>
      </div>

      <!-- <div class="hero-image">
  <div class="hero-text">
    <h1>I am John Doe</h1>
    <p>And I'm a Photographer</p>
    <button>Hire me</button>
  </div> -->

</template>

<script>
export default {
    name: "Hero"
}
</script>

<style>
#hero-image {
    background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("../assets/images/lobby.jpg");
    background-position: center;
}
/* body, html {
    height: 100%;
}


.hero-image {
  
  background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("/assets/images/lobby.jpg");


  height: 50%;

 
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
}

.hero-text {
  text-align: center;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: white;
} */
</style>