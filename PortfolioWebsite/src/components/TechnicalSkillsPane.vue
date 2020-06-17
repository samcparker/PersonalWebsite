<template>
  <section>
      <h1 class="display-3">Technical Skills</h1>
       <p class="lead  mt-4"><em>Here are some of my technical skills.</em></p>
        <div class="px-3">
            <technical-skills-section v-for="(itemList, index) in items" :key="index" :itemList="itemList" :title="index"></technical-skills-section>
        </div>
  </section>
</template>

<script>
import TechnicalSkillsSection from "./TechnicalSkillsSection.vue"

export default {
    name: "TechnicalSkills",
    data: function() {
        return {
            items: {
                "Programming": [
                    {
                        name: "Java",
                        text: "Java is one of my all time favourite languages and what got me into programming the most. I have spent a lot of time using the Graphics2D package to create games.",
                    },
                    {
                        name: "Lua",
                        text: "I became very fond of Lua when using it to develop games on the ROBLOX platform. I enjoy it for its simplicity and easiness to understand.",
                    },
                    {
                        name: "Python",
                        text: "Python is one of the first languages I learned and has come to be one of my favourites.",
                    }
                ],
                "Web Development": [
                    {
                        name: "HTML, CSS & JS",
                        text: "The fundamentals of web development.",
                    },
                    {
                        name: "Vue.js",
                        text: "Vue.js is the first react framework that I touched upon and I am looking forward to using it more. This website was made in Vue.js!",
                    },
                    {
                        name: "MVC Frameworks",
                        text: "The first MVC framework I used was CodeIgniter for a coursework project. I have also worked with Django.",
                    },
                    {
                        name: "Bootstrap",
                        text: "CSS was one of the least favourite parts of web development for me, and that is why I am so glad to have come across Bootstrap. Even this website was made with it!",
                    },
                ],
               
            }
            
        }
    },
    components: {
    TechnicalSkillsSection
  }
}
</script>

<style>

</style>