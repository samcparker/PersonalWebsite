<template>
    <li class="list-group-item content-field px-3">
        <div class="">
            
            <div class="row">
                <div class="col-md">
                    <h2 class="display-4 text-break">{{ project_title }}</h2>
                    <p class="lead text">{{ project_text }}</p>
                    <a class="text-center mb-5" :href="project_github_link" target="_blank">Source on Github</a>
                </div>
                <div class="col-md justify-content-center d-flex   my-auto">
                    <img :src="require('@/assets/images/' + project_image + '')"
                        class="mt-3 img-fluid ${3|rounded-top,rounded-right,rounded-bottom,rounded-left,rounded-circle,|}"
                        alt="Project image">
                </div>
            </div>
        </div>

    </li>
</template>

<script>
    export default {
        name: "ProjectItem",
        props: {
            project_title: String,
            project_text: String,
            project_github_link: String,
            project_image: String,
        },
    }
</script>

<style>

</style>