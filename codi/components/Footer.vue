<template>
    <v-card 
        title
        flat
        rounded="lg"
        class="pa-md-5 pa-3 text-center"
        color="surface"
        >
        <h2 class="text-md-h6 font-weight-bold">Atlas-Expo</h2>
        <p class="text-md-body-2 mt-5">Free eCommerce Website Built With NuxtJs ❤</p>
        <div>
            <v-btn v-for="(s, i) in sm" :key="`socialMedia-${i}`"
                icon fab class="mr-2">
                <v-icon 
                    size="30"
                    depressed
                    >{{s.icon}}</v-icon>
            </v-btn>
        </div>
    </v-card>
</template>
<script>
export default{
    data(){
        return{
            sm:[
                {
                    icon:"mdi-facebook", Link: "https://www.facebook.com",
                },
                {
                    icon:"mdi-instagram", Link: "https://www.instagram.com",
                },
                {
                    icon:"mdi-twitter", Link: "https://www.twitter.com",
                },
                {
                    icon:"mdi-youtube", Link: "https://www.youtube.com",
                },
            ]
        }
    }
}
</script>