<template>
<div>
        <h1 class="display-3">Latest Blog Posts [coming soon!]</h1>
        <v-list>
            <v-list-item v-for="(blog, i) in posts" :key="i" class="pb-10 mb-10"
                style="border-bottom: 1px solid black">
                <blog-small :blog="blog"></blog-small>
            </v-list-item>
        </v-list>
</div>

</template>


<script>
import BlogSmall from '@/components/BlogSmall.vue'

export default {
    name: "Blog",
    components: {BlogSmall},
data: () => {
        return {
            posts: [
                {
                    title: "How I made a top-nav bar using Vuetify",
                    contents: "Hey fellas, this is how I made a top-nav bar in Vuetify etc.....",
                    link: "#",
                    blog_image: "icon.png"
                },
                {
                    title: "Why I use Vue.js over React",
                    contents: "Hey fellas, this is how I made a top-nav bar in Vuetify etc.....",
                    link: "#",
                    blog_image: "icon.png"
                },
            ]
        }
    }
}
</script>

<style>

</style>