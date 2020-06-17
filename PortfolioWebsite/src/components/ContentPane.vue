<template>
  <section>
      <h1 class="text-left display-3">{{ title }}</h1>
      <p class="lead  mt-4"><em>A little bit about me...</em></p>
      <div class="px-3">
          <p class="lead">My name is Sam and I study computer science at the University of Kent.</p>
          <p class="lead">I love to bake, watch films and (most of all) write programs on my computer.</p>

          </div>
  </section>
</template>

<script>
export default {
    name: "ContentPane",
    props: {
        title: String,
        text: String,
    }
}
</script>

<style>

</style>