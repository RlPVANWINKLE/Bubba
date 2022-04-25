<template>
    <v-form  v-model="valid" class="grey darken-4 " ref="form">
    <v-container fluid class=" font-weight-bold mx-auto ">
        <v-card  class="mx-auto my-16 py-10 myclass"  >
            <h1 class="text-center text-decoration-underline">About You</h1>
        <v-row align="center" justify="center">
            <v-col cols="5" md="3">
            <v-text-field
                v-model="firstname"
                :rules="nameRules"
                :counter="10"
                label="First name"
                required
            ></v-text-field>
            </v-col>
            <v-col cols="5" md="3">
            <v-text-field
                v-model="lastname"
                :rules="nameRules"
                :counter="10"
                label="Last name"
                required
            ></v-text-field>
            </v-col>
            <v-col cols="10" md="3">
            <v-text-field
                v-model="email"
                :rules="emailRules"
                label="E-mail"
                required
            ></v-text-field>
            </v-col>
        </v-row>
        <v-row align="center"
      justify="center">
          <v-col cols="10" md=4>
            <v-text-field
            v-model="address"
            :rules="addRules"
            :counter="20"
            label="Address"
            required
          ></v-text-field>
          </v-col>
          <v-col cols="5" md=3>
            <v-text-field
            v-model="zip"
            :rules="zipRules"
            :counter="5"
            label="ZipCode"
            required
          ></v-text-field>
          </v-col>
          <v-col cols="5" md=2>
            <v-select
            v-model="select"
            :hint="`${select.state}, ${select.abbr}`"
            :items="items"
            item-text="state"
            item-value="abbr"
            label="Select"
            persistent-hint
            return-object
            single-line
            ></v-select>
          </v-col>
      </v-row>
      <v-row align="center"
      justify="center"> 
          <v-col cols="8" md=9> 
            <v-radio-group v-model="radioGroup" row>
            <v-radio
            :label="`Rent`"
            ></v-radio>
            <v-radio
            :label="`Rent-To-Own`"
            ></v-radio>
            <v-radio
            :label="`Mortgage`"
            ></v-radio>
            <v-radio
            :label="`Own`"
            ></v-radio>
            </v-radio-group>
          </v-col>
      </v-row>
        <h1 class="text-center text-decoration-underline">About Your House</h1>
        <v-row align="center" justify="center">
            <v-col cols="10" md=3>
                <v-select
                v-bind="bedrooms"
                :items="roomscnt"
                label="Number of Bedrooms"
                ></v-select>
            </v-col>
            <v-col cols="10" md=3>
                <v-select
                v-bind="bedheight"
                :items="height"
                label="Bedroom Height"
                ></v-select>
            </v-col>
            <v-col cols="10" md=3>
                <v-select
                v-bind="bathrooms"
                :items="roomscnt"
                label="Number of Bathrooms"
                ></v-select>
            </v-col>         
            
        </v-row>
        <v-row align="center" justify="center">
            <v-col cols="10" md=4>
                <v-select
                v-bind="greatrooms"
                :items="Groomscnt"
                label="Number of Great Rooms"
                ></v-select>
            </v-col>
            <v-col cols="10" md=4>
                <v-select
                v-bind="groomheight"
                :items="height"
                label="Great Room Height (AVG)"
                ></v-select>
            </v-col>
            </v-row>
            <v-row align="center" justify="center">
                <v-col cols="10" md="9">
                    <v-textarea
                        v-model="comments"
                        :rules="textRules"
                        :counter="250"
                        label="Additional Comments"
                        filled
                    ></v-textarea>
                </v-col>
            </v-row>
            <v-row align="center" justify="center" @click="submit(firstname)">
                <v-btn color="#FFC107">
                    Submit
                </v-btn>
            </v-row>    
        </v-card>
    </v-container>
  </v-form>
</template>
<script>
import items from '../components/states.js'
  export default {
    data(){
        return{
            select: {state: 'Florida', abbr: 'FL'},
            items: items,
            valid: false,
            firstname: '',
            lastname: '',
            nameRules: [
                v => !!v || 'Name is required',
                v => v.length <= 10 || 'Name must be less than 10 characters',
            ],
            email: '',
            emailRules: [
                v => !!v || 'E-mail is required',
                v => /.+@.+/.test(v) || 'E-mail must be valid',
            ],
            textRules:[
                v => v.length <= 250 || 'Please keep under 250 characters'
            ],
            address: '',
            roomscnt: ['1','2','3','4','5','6'],
            Groomscnt: [1,2,3],
            height:['8ft','10ft','12ft','15ft','20ft','25ft','30ft'],
            bedrooms: '1',
            bathrooms: '1',
            greatrooms: '1',
            bedheight: '8ft',
            comments: ''
        }
    },
    methods:{
        submit(firstname){
            alert('Thank-you ' + firstname.toUpperCase() + '. We will get back to you within 48 business hours!')
            this.$refs.form.reset();
        }
    }
  }
</script>
<style scoped>
.myclass.v-sheet.v-card{
    border: 8px solid #FFC107;
}
@media only screen and (max-width: 600px) {
    .myclass{
        width: 95%;
    }
}
@media only screen and (max-width: 1500px) {

}
@media only screen and (min-width: 600px) {
    .myclass{
        width: 60%;
    }
}
</style>