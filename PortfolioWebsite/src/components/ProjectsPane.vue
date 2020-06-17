<template>
    <section>
        <h1 class="text-left display-3">Projects</h1>
        <p class="lead  mt-4"><em>A list of projects that I've been working on.</em></p>
        <ul class="list-group list-group-flush">
                    <project-item v-for="project in projects" :key="project.id" :project_title="project.title"
            :project_text="project.text" :project_image="project.image" :project_github_link="project.github_link">
        </project-item>
        </ul>

    </section>
</template>

<script>
    import ProjectItem from "./ProjectItem.vue"
    export default {
        name: "ProjectsPane",
        components: {
            ProjectItem
        },
        data: function () {
            return {
                projects: [{
                        id: 1,
                        title: "Portfolio Website",
                        text: "I recently decided it was time to create a portfolio website - so here it is! It uses Vue.js and Bootstrap and was very enjoyable to create. ",
                        image: "sample.jpg",
                        github_link: "https://github.com/juicehub/PortfolioWebsite"
                    },
                {
                        id: 1,
                        title: "Java Circle Drawing",
                        text: "I was told from a good friend of mine about a game in which you had to draw a circle and get it as accurate as possible. Having skills in Java's Robot class, I decided to automate the process so I could draw perfect circles every time. Check out the Github page to see how it works and a GIF of it in action.",
                        image: "circle_draw.jpg",
                        github_link: "https://github.com/juicehub/JavaCircle"
                    },

                ]
            }
        },
    }
</script>

<style>

</style>