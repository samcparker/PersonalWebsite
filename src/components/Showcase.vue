<template>
<div>
        <h1 class="display-3">Latest Projects</h1>
        <v-list>
            <v-list-item v-for="(project, i) in projects.slice(0,amount)" :key="i" class="pb-10 mb-10"
                style="border-bottom: 1px solid black">
                <project-small :project="project"></project-small>

            </v-list-item>
        </v-list>
        <v-row>
            <div justify="center">
                <v-btn v-if="projects.length != amount" @click="amount++" class="ml-2" color="primary" large>See More
                </v-btn>
                <v-btn v-else @click="addItem" class="ml-2" color="primary" large disabled>See More
                </v-btn>
            </div>
        </v-row>
        </div>


</template>

<script>
    import ProjectSmall from '@/components/ProjectSmall.vue';
    import { db } from '@/main';
    export default {
        name: "Showcase",
        components: {ProjectSmall},
        mounted() {
            this.getProjects();
        },
        methods: {
            addItem() {
                    amount++;
                    // TODO : add code so that it auto scrolls to new item
       
                },
            async getProjects() {
                console.log("hi");
                let snapshot = await db.collection('projects').get();
                let projects = [];
                snapshot.forEach(doc => {
            
                    projects.push(doc.data());
                });
      
                this.projects = projects;
            }
        },

        data: () => {
            return {
                amount: 2,
                projects: [],
                // projects: [{
                //         title: "Java Circle Drawing",
                //         caption: "A short bit of code used to move the mouse around in a circle.",
                //         icons: [{
                //             mdi: "mdi-language-java",
                //             tooltip: "Java"
                //         }],
                //         live_demo: "disabled",
                //         github: "https://github.com/samcparker/JavaCircle",
                //         project_image: "circle.jpg"
                //     },
                //     {
                //         title: "Personal Website",
                //         caption: "Finally made a portfolio website! [this one that you're using!]",
                //         icons: [{
                //             mdi: "mdi-vuejs",
                //             tooltip: "Vue.js"
                //         }, {
                //             mdi: "mdi-vuetify",
                //             tooltip: "Vuetify"
                //         }, 
                //         {
                //             mdi: "mdi-language-html5",
                //             tooltip: "HTML5"
                //         },
                //         {
                //             mdi: "mdi-firebase",
                //             tooltip: "Firebase"
                //         }
                //         ],
                //         live_demo: "https://www.samcparker.co.uk",
                //         github: "https://www.github.com/samcparker/PortfolioWebsite",
                //         project_image: "icon.png"
                //     },
                //     {
                //         title: "Portfolio Website",
                //         caption: "I have finally made my portfolio website!",
                //         icons: [{
                //             mdi: "mdi-vuejs",
                //             tooltip: "Vue.js"
                //         }, {
                //             mdi: "mdi-vuetify",
                //             tooltip: "Vuetify"
                //         }, {
                //             mdi: "mdi-language-html5",
                //             tooltip: "HTML5"
                //         }],
                //         live_demo: "https://www.samcparker.co.uk",
                //         github: "https://www.github.com/samcparker/PortfolioWebsite",
                //         project_image: "website_sample.png"
                //     },
                //     {
                //         title: "Portfolio Website",
                //         caption: "I have finally made my portfolio website!",
                //         icons: [{
                //             mdi: "mdi-vuejs",
                //             tooltip: "Vue.js"
                //         }, {
                //             mdi: "mdi-vuetify",
                //             tooltip: "Vuetify"
                //         }, {
                //             mdi: "mdi-language-html5",
                //             tooltip: "HTML5"
                //         }],
                //         live_demo: "https://www.samcparker.co.uk",
                //         github: "https://www.github.com/samcparker/PortfolioWebsite",
                //         project_image: "website_sample.png"
                //     },
                //     {
                //         title: "Portfolio Website",
                //         caption: "I have finally made my portfolio website!",
                //         icons: [{
                //             mdi: "mdi-vuejs",
                //             tooltip: "Vue.js"
                //         }, {
                //             mdi: "mdi-vuetify",
                //             tooltip: "Vuetify"
                //         }, {
                //             mdi: "mdi-language-html5",
                //             tooltip: "HTML5"
                //         }],
                //         live_demo: "https://www.samcparker.co.uk",
                //         github: "https://www.github.com/samcparker/PortfolioWebsite",
                //         project_image: "website_sample.png"
                //     },
                //     {
                //         title: "Portfolio Website",
                //         caption: "I have finally made my portfolio website!",
                //         icons: [{
                //             mdi: "mdi-vuejs",
                //             tooltip: "Vue.js"
                //         }, {
                //             mdi: "mdi-vuetify",
                //             tooltip: "Vuetify"
                //         }, {
                //             mdi: "mdi-language-html5",
                //             tooltip: "HTML5"
                //         }],
                //         live_demo: "https://www.samcparker.co.uk",
                //         github: "https://www.github.com/samcparker/PortfolioWebsite",
                //         project_image: "website_sample.png"
                //     },
                // ]
            }
            
        }

    }
</script>

<style>

</style>