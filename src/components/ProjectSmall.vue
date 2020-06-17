<template>
    <v-row style="max-width: 100%">
        <v-col sm="12" md="5">
            <v-img style="max-height: 10rem" :src="require('@/assets/images/' + project.project_image + '')">

            </v-img>
        </v-col>
        <v-col sm="12" md="7">
            <v-row class="flex-column">
                <div>


                    <v-tooltip v-for="(icon, j) in project.icons" :key="j" bottom>
                        <template #activator="{ on }">
                            <v-chip class="mr-2" v-on="on">
                                <v-icon color="grey" class="mr-1">{{ icon.mdi }}</v-icon>
                            </v-chip>

                        </template>
                        <span>{{ icon.tooltip }}</span>
                    </v-tooltip>
                </div>
                <h1>{{ project.title }}</h1>
                <p>{{ project.caption }}</p>

                <div class="mt-1">
                    <v-row>
                        <v-col>
                            <v-btn :href="project.github" target="_blank" class="mr-2" color="primary" outlined>Github
                                <v-icon right>
                                    mdi-github
                                </v-icon>
                            </v-btn>
                        </v-col>
                        <v-col>
                            <v-btn v-if="project.live_demo != 'disabled'" :href="project.live_demo" target="_blank"
                                class="" color="primary">Live Demo<v-icon right>
                                    mdi-television</v-icon>
                            </v-btn>

                            <v-btn v-else="" target="_blank" class="" color="primary" disabled>Live Demo<v-icon
                                    right>
                                    mdi-television</v-icon>
                            </v-btn>
                        </v-col>
                    </v-row>








                </div>

            </v-row>
        </v-col>

    </v-row>
</template>

<script>
    export default {
        name: "ProjectSmall",
        props: {
            project: Object
        }
    }
</script>

<style>

</style>