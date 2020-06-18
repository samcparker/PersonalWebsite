<template>
    <v-row style="max-width: 100%">
        <v-col xs="12" sm="12" md="5" lg="5" xl="5">
            <!-- <v-img style="max-height: 10rem" :src="require('@/assets/images/' + project.project_image + '')">

            </v-img> -->
            <v-img v-if="img_src" style="max-height: 10rem" :src="img_src">

            </v-img>
            <v-img v-else style="max-height: 10rem" src="@/assets/images/logo.png" gradient="to top right, rgba(100,115,201,.33), rgba(25,32,72,.7)">
                <v-row class="flex-column" justify="center" align="center" style="height: 100%; max-width: 100%">
                    <h1 class="display-1 white--text">Image not found!</h1>
                    <p class="white--text">Sorry about that.</p>
                </v-row>
                
            </v-img>
        </v-col>
        <v-col xs="12" sm="12" md="7" lg="7" xl="7">
            <v-row class="flex-column">
                <div>


                    <v-tooltip v-for="(icon, j) in project.icons" :key="j" top>
                        <template #activator="{ on }">
                            <v-chip class="mr-2" v-on="on">
                                <v-icon color="grey" class="mr-1">{{ icon }}</v-icon>
                            </v-chip>

                        </template>
                        <span>{{ j }}</span>
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
import {
        db,
        storage
    } from '@/main';

export default {
    name: "ProjectSmall",
    props: {
        project: Object
    },
    data: () => {
        return {
            img_src: null,
        }
    },
    methods: {
        setImage(i) {
            console.log("URL: " + i);
            storage.refFromURL(i).getDownloadURL().then(this.assignSrc);
        },
        assignSrc(src) {
            this.img_src = src;
            console.log(this.img_src);
        }
    },
    created() {
        if (this.project.image) {
            this.setImage(this.project.image);
        }
        
        console.log(this.project);

        
    }
}
</script>

<style>

</style>