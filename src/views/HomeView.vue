<template>
  <div class="grey darken-4 ">
    <v-card
      class="d-flex align-center justify-center py-16 mx-auto amber"
      max-width=100%
      outlined
    >
      <div class="text--- font-weight-black font-lato">
        Bubba's Painting
      </div>
    </v-card>
    
    <v-container  class=" text-center mb-3 mt-16" >
      <h1 class=" display-cust py-3 amber">Current Home Styles</h1>
      <v-carousel cycle hide-delimiters :show-arrows="true" class="grey ">
        <v-carousel-item
          v-for="(item,i) in items"
          :key="i"
          :src="item.src"
          reverse-transition="fade-transition"
          transition="fade-transition"
          class=" d-flex align-center justify-center sml"
          max-width=100%  
          contain        
        ></v-carousel-item>
      </v-carousel>
    </v-container>
    
    <v-container class=" py-5 text-center">
      <h1 class=" display-cust py-3 amber">About Bubba's Painting</h1>
      <div class="d-flex grey mb-3 under ">
        <v-img src="../images/KYLE.jpg" class="caros"></v-img>
        <p class="text-center pt-5 text-- ">Bubba's painting has been in business for 22 years as of March of 2022. We have been throughout some small cities in the united states. Our most recent city was in a small city of Florida. We have since moved to the State of Utah and have been painting homes throughout the northern quarter of the state. The founder was a man by the name of Steve Hulshen. Steve has since passed and the company passed to his son, Kyle. Kyle has succesfully ran the business for the last 12 years, and has been painting homes since the age of 8. While this wasnt what he imagined his future being, he is happy to have this as his life and foreseable future.  </p>
      </div>
      
    </v-container>
  </div>
  
</template>

<script>
  import items from '../components/NewHomes.js'

  export default {
    name: 'HomeView',

    components: {
      // HelloWorld,
    },
    data(){
      return{
        items: items,
      }
    }
  }
</script>
<style scoped>
@media only screen and (max-width: 600px) {
  .text---{
    font-size:3.0rem ;
  }
  .text--{
    font-size: 1rem;  
    margin-right: 25px;
    margin-left: 25px;
  }
  .caros{
   height: 10%;
   width: 100%;
  }
  .under{
    display: flex;
    flex-wrap: wrap;
  }
}
@media only screen and (max-width: 1500px) {
  .caros{
   height: 10%;
   width: 100%;
  }
  .under{
    display: flex;
    flex-wrap: wrap;
  }
}

@media only screen and (min-width: 600px) {
  .text---{
    font-size:6rem ;
  }
  .display-cust{
    font-size: 3.75rem;
  }
  .text--{
    font-size: 2.125rem;  
    margin-right: 25px;
    margin-left: 25px;
  }
}
</style>
