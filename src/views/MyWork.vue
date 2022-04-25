<template>
    <div class="grey darken-4 ">
        <PopUp v-show="isModalVisible" @close="closeModal">
            <template v-slot:header>
                {{header}} Information
            </template>

            <template v-slot:body>
                
                    <v-container fluid class="under">
                        <v-carousel cycle  :show-arrows="true" class="grey">
                            <v-carousel-item
                            v-for="(item,i) in items"
                            :key="i"
                            :src="item"
                            reverse-transition="fade-transition"
                            transition="fade-transition"
                            class=" d-flex align-center justify-center"
                            contain                            
                                  
                            ></v-carousel-item>
                        </v-carousel>
                    </v-container>
                
            </template>

            <template v-slot:footer>
                The total time taken to finish this project was {{time}}! It cost a total of {{cost}}! Interested?
            </template>
        </PopUp>
        <v-container fluid class=" justify-center align-center" v-show="main">
                <v-row>
                    <v-col cols="12" md=3 v-for="(home, index) in homes" :key="index" >
                        <v-card height="80%" class="mx-auto my-12 myclass" >
                            <v-img max-width="100%" max-height="70%" :src="home.pic" @click="showModal(); modalcontent(home)"></v-img>
                            <v-card-subtitle class="text-center" > Project Cost: {{home.cost}}</v-card-subtitle>
                            <v-card-subtitle class="text-center"> Time to completion: {{home.time}}</v-card-subtitle>
                            
                        </v-card>
                    </v-col>
                </v-row>
        </v-container>
    </div>
</template>
<script>

import PopUp from '../components/PopUp.vue'

import homes from '../components/HomeData.js'
export default {
    name:"MyWork",
    components:{
        PopUp,
    },    
    methods: {
      showModal() {
        this.isModalVisible = true;
        this.main = false;
      },
      closeModal() {
        this.isModalVisible = false;
        this.main = true;
      },
      modalcontent(home){
        this.header = home.prefix;
        this.items = home.gallery;
        this.time = home.time;
        this.cost = home.cost;
        
      }
    },
    data(){
        return{
            homes: homes,
            isModalVisible: false,
            header: "",
            items: [],
            main: true,
            cost: '',
            time: ''
        }
    },
}

</script>
<style scoped>
.myclass.v-sheet.v-card{
    border: 8px solid #FFC107;
}
.myclass.v-sheet.v-card:hover{
    cursor: pointer;
}
@media only screen and (max-width: 600px) {
 .myclass{
   max-width: 90%;
 }
 .under{
     max-width: 90%;
     max-height: 50%;
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
