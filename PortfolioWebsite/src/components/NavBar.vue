<template>

  <nav class="navbar custom-navbar navbar-expand-lg navbar-dark shadow fixed-top">
    <div class="container">

      <button class="navbar-toggler d-lg-none" type="button" data-toggle="collapse" data-target="#collapsibleNavId"
        aria-controls="collapsibleNavId" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="collapsibleNavId">
        <ul class="navbar-nav nav-fill w-100 mt-2 mt-lg-0">
          <li class="nav-item"><a class="nav-link" href="#home">Home</a></li>
          <li class="nav-item"><a class="nav-link" href="#about">About Me</a></li>
          <li class="nav-item"><a class="nav-link" href="#projects">Projects</a></li>
          <li class="nav-item"><a class="nav-link" href="#technical">Technical Skills</a></li>
          <li class="nav-item"><a class="nav-link" href="#contact">Contact</a></li>

        </ul>
      </div>

    </div>
  </nav>

</template>

<script>
  export default {
    name: "NavBar"
  }
</script>

<style>
  .custom-navbar {
    background-color: #1EA9AC;
  }
</style>