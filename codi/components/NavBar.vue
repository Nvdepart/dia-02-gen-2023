<template>
    <div>
        <v-app-bar
            color="surface"
            height="80" 
            class="el" 
            app 
            :style="{padding : $vuetify.breakpoint.mdAndUp ? '0px 100px' : ''}"
        >
            <v-toolbar-title
                @click="$router.push('/')" 
                class="text-md-h5 font-weight-bold pointer"   
                >
                <v-icon size="30" color="blue">mdi-atlassian</v-icon>
                tlas-Expo
            </v-toolbar-title>
            <v-spacer />
            <v-btn icon>
                <v-icon size="30" color="yellow">mdi-store-outline</v-icon>
            </v-btn>
            <v-btn icon>
                <v-icon size="30" color="green">mdi-cart-outline</v-icon>
            </v-btn>
            <v-divider vertical class="mx-md-5 mx-2"/>
            <v-btn @click="toggleTheme" icon>
                <v-icon size="30" color="red">mdi-brightness-4</v-icon>
            </v-btn>
        </v-app-bar>
    </div>
</template>
<script>
export default {
    methods: {
        toggleTheme() {
        this.$vuetify.theme.dark = !this.$vuetify.theme.dark;
        },
  },
}
</script>