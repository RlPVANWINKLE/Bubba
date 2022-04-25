<template>
  <div class="about grey darken-4 ">
    <v-container class="justify-center align-center">
      <h1 class=" text-center display-2 py-3 white--text">Meet Our Crew</h1>
      <v-row>
        <v-col cols="12" md="4">
          <v-card class="mx-auto my-12 myclass">
            <v-img  src="../images/kyle2.jpg" width="100%" class="mx-auto"></v-img>
            <v-card-title class="text-center display-1 ">Kyle</v-card-title>   
            <v-card-subtitle class="">Owner</v-card-subtitle>
            <v-card-text class="">Kyle is the current owner of Bubba's Painting. He has been paintign from a very young age, taught to him by his father. He knows many if not all the current trends and styles of the paint world. Whether that bne indoor or outdoor painting.</v-card-text>
          </v-card>
        </v-col>
        <v-col cols="12" md="4">
          <v-card class="mx-auto my-12 myclass">
            <v-img  src="../images/tyler.jpg" width="100%" class="mx-auto"></v-img>
            <v-card-title class="text-center display-1 ">Tyler</v-card-title>   
            <v-card-subtitle class="">Finance Manager</v-card-subtitle>  
            <v-card-text>Tyler is the Finance Manager for Bubba's painting. He has been in this position for almost 10 years! Tyler may not know all the tips and tricks of painting a home, however he knows how to create success and happy clients.</v-card-text>
          </v-card>
        </v-col>
        <v-col cols="12" md="4">
          <v-card class="mx-auto my-12 myclass">
            <v-img  src="../images/eric.jpg" width="100%" class="mx-auto"></v-img>
            <v-card-title class="text-center display-1 ">Eric</v-card-title>   
            <v-card-subtitle class="">Home Inspection</v-card-subtitle>  
            <v-card-text>Eric is the Home Inspector for Bubba's painting. He is the one who you as a customer will talk to for any issues with the project. He will happily assist and make sure that your needs are met. Eric is always on your side.</v-card-text>
          </v-card>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12" md="4">
          <v-card  class="mx-auto my-12 myclass">
            <v-img  src="../images/greage.jpg" width="100%" class="mx-auto"></v-img>
            <v-card-title class="text-center display-1 ">Greage</v-card-title>   
            <v-card-subtitle class="">Supplies Manager / Painter</v-card-subtitle>
            <v-card-text>Greage is our newest employee, he has been hired to learn to paint as well as maintain the supplies within the shop. He handles inventory for all the supplies that the painters use on a day to day basis. </v-card-text>  
          </v-card>
        </v-col>
        <v-col cols="12" md="4">
          <v-card  class="mx-auto my-12 myclass">
            <v-img  src="../images/porter.jpg" width="100%" class="mx-auto"></v-img>
            <v-card-title class="text-center display-1 ">Porter</v-card-title>   
            <v-card-subtitle class="">Painter</v-card-subtitle>  
            <v-card-text>Porter is detail painter. Porter goes to homes after they have been "mass-painted". And goes through with a paintbrush and roller in order to get all the tiny details that a sprayer may miss due to its pressure.</v-card-text>
          </v-card>
        </v-col >
        <v-col cols="12" md="4">
          <v-card class="mx-auto my-12 myclass">
            <v-img  src="../images/kyler.jpg" width="100%" class="mx-auto"></v-img>
            <v-card-title class="text-center display-1 ">Kyler</v-card-title>   
            <v-card-subtitle class="">Painter</v-card-subtitle> 
            <v-card-text>Kyler is our mass painter. Kyler goes to each home and masks all the objects and places off, that are not to be painted. He then has the training and expertise to use a sprayer for a quick application of paint.</v-card-text> 
          </v-card>
        </v-col>
      </v-row>
      
    </v-container>
  </div>
</template>

<style scoped>
.myclass.v-sheet.v-card{
    border: 8px solid #FFC107;
}
@media only screen and (max-width: 600px) {
 .myclass{
   max-width: 90%;
 }
}
@media only screen and (max-width: 1500px) {

}
@media only screen and (min-width: 600px) {
  .myclass{
   max-width: 70%;
 }
}
</style>
