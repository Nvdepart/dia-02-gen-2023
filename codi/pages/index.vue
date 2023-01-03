<template>
<v-container>
  <NavBar />
  <v-row>
    <v-col>
      <h1 class="animate__zoomInDown">Atlas Expo</h1>
    </v-col>
    <HomeCarousel />
    <NewsLetters />
  </v-row>
  <Footer />
</v-container>
</template>

<script>
import 'animate.css'
export default {
  name: 'IndexPage',
  async created(){
    this.sale_items= await this.$content("products").where({onSale:true}).fetch();
    this.products= await this.$content("products").fetch();
  },
  data(){
    return{
      products: null,
      sale_items: null,
    }
  }
}
</script>