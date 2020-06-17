<template>
  <div>
    <h2 class="display-4">{{ title }}</h2>
    <div class="row my-4">
        <technical-skills-item class="col-lg-4 col-md-6" v-for="item in itemList" :key="item" :name="item.name" :text="item.text"></technical-skills-item>
    </div>
    
  </div>
</template>

<script>
import TechnicalSkillsItem from "./TechnicalSkillsItem.vue"

export default {
    name: "TechnicalSkillsArea",
    props: {
        title: String,
        itemList: Array
    },
    components: {
        TechnicalSkillsItem
    }
}
</script>

<style>

</style>