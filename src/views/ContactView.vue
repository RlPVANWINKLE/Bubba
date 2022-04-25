<template>
    <v-form class="grey darken-4 ">
        <v-container>
            <v-card class="mx-auto my-16 py-10 myclass">
                <h1 class="text-center text-decoration-underline">How Can We Help You?</h1>
                <v-row align="center" justify="center">
                    <v-col cols="5" md="5">
                        <v-text-field
                        v-model="firstname"
                        :rules="nameRules"
                        :counter="10"
                        label="First Name"
                        required>
                        </v-text-field>
                    </v-col>
                    <v-col cols="5" md="5">
                        <v-text-field
                        v-model="lastname"
                        :rules="nameRules"
                        :counter="10"
                        label="Last Name"
                        required>
                        </v-text-field>
                    </v-col>
                </v-row>
                <v-row align="center" justify="center">
                    <v-col cols="5" md="5">
                        <v-text-field
                        v-model="email"
                        :rules="emailRules"
                        label="E-mail"
                        required>
                        </v-text-field>
                    </v-col>
                    <v-col cols="5" md="5">
                        <v-text-field
                        v-model="phone"
                        :rules="phoneRules"
                        label="Phone Number"
                        required>
                        </v-text-field>
                    </v-col>
                </v-row>
                <v-row align="center" justify="center">
                <v-col cols="10" md="10">
                    <v-textarea
                        v-model="comments"
                        :rules="textRules"
                        :counter="250"
                        label="Additional Comments"
                        filled
                    ></v-textarea>
                </v-col>
            </v-row>
            </v-card>
        </v-container>
        <v-container>
            <v-card class="mx-auto my-8 py-10 myclass">
             <h1 class="text-center text-decoration-underline">Contact Us Today!!!</h1>
             <v-row align="center" justify="center" class="">
                 <v-col cols="8" md="5">
                     <v-card-subtitle class="text-center text---">Our Phone Number: <br> (801)647-6433</v-card-subtitle>
                 </v-col>
                 <v-col cols="8" md="5">
                     <v-card-subtitle class="text-center text---">Our E-mail: BubbasPainting@gmail.com</v-card-subtitle>
                 </v-col>
             </v-row>
             <h2 class="text-center text-decoration-underline">Our Hours</h2>
             <v-row align="center" justify="center" class="">
                 <v-col cols="8" md="5">
                    <v-card-subtitle class="text-center text---" >MON-FRI: 8:00AM - 6:00PM</v-card-subtitle>
                    <v-card-subtitle class="text-center text---" >SAT & SUN: Closed</v-card-subtitle>
                </v-col>
             </v-row>
             
            </v-card>
        </v-container>
    </v-form>
</template>

<script>
export default {
    data(){
        return{
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
.text---{
    font-size: .95rem;
}
}
@media only screen and (max-width: 1500px) {

}
@media only screen and (min-width: 600px) {
.myclass{
    width: 60%;
}
.text---{
    font-size: 1.50rem;
}
}
</style>