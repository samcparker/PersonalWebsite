<template>
  <div>
      <p><strong>{{ name }}</strong></p>
      <p class="lead">{{ text }}</p>
  </div>
</template>

<script>
export default {
    name: "TechnicalSkillsItem",
    props: {
        name: String,
        text: String,
    }
}
</script>

<style>

</style>