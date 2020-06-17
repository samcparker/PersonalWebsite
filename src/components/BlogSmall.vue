<template>
    <v-row style="max-width: 100%">
        <v-col cols="5">
            <v-img style="max-height: 10rem" :src="require('@/assets/images/' + blog.blog_image + '')">

            </v-img>
        </v-col>
        <v-col cols="7">
            <v-row class="flex-column">
                <h1>{{ blog.title }}</h1>
                <p>{{ blog.contents }}</p>

                <div class="mt-1">
                    <v-btn :href="blog.link" class="mr-2" color="primary" disabled>Full Post<v-icon right>
                            mdi-post
                        </v-icon>
                    </v-btn>

                </div>

            </v-row>
        </v-col>

    </v-row>

</template>

<script>
    export default {
        name: "BlogSmall",
        props: {
            blog: Object
        }
    }
</script>

<style>

</style>