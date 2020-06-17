<template>
    <div>
        
        <v-navigation-drawer v-model="drawer" temporary absolute class="hidden-md-and-up fill-height">
            <v-list dense nav>
                <v-list-item v-for="(link, index) in links" :key="index" link>
                    <v-list-item-action>
                        <v-icon>{{ link.icon }}</v-icon>
                    </v-list-item-action>
                    <v-list-item-content>
                        <v-list-item-title>
                            {{ link.title }}
                        </v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>
        <v-app-bar app flat>
            <v-app-bar-nav-icon
            class="d-flex d-md-none"
            @click="drawer = !drawer"></v-app-bar-nav-icon>
            <v-toolbar-title>Portfolio</v-toolbar-title>
            <v-btn v-for="(link, index) in links" :key="index" class="hidden-sm-and-down">{{ link.title }}</v-btn>
        </v-app-bar>

    </div>

</template>

<script>
    export default {
        name: "NavBar",
        data: () => {
            return {
                drawer: false,
                links: [{
                        title: "Title1",
                        icon: "mdi-cog"
                    },
                    {
                        title: "Title2",
                        icon: "mdi-cog"
                    },
                    {
                        title: "Title3",
                        icon: "mdi-cog"
                    },
                ]
            }
        }
    }
</script>

<style>

</style>