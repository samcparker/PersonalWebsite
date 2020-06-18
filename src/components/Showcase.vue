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
    import {
        db,
        storage
    } from '@/main';
    export default {
        name: "Showcase",
        components: {
            ProjectSmall
        },
        mounted() {
            this.getProjects();
        },
        methods: {

            addItem() {
                amount++;
                // TODO : add code so that it auto scrolls to new item

            },
            async getProjects() {
                let snapshot = await db.collection('projects').get();
                let projects = [];


                snapshot.forEach(doc => {
                    let data = doc.data();
                    projects.push(data);
                });

                this.projects = projects;
            }
        },

        data: () => {
            return {
                amount: 2,
                projects: [],
            }

        }

    }
</script>

<style>

</style>