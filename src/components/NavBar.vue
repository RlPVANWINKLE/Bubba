<template>
    <nav >
        <v-toolbar app>
            <v-app-bar-nav-icon @click="menu = !menu"></v-app-bar-nav-icon>
            <v-toolbar-title class="text-uppercase">
                <span class="font-weight-bold amber--text under">Bubba's</span>
                <span class=" grey--text under-1">Painting</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <span><router-link to="/contact" class="text-decoration-none ">Contact Us</router-link></span>
        </v-toolbar> 
        <v-navigation-drawer app v-model="menu" class="grey lighten-2" >
          <v-img  src='../images/painting.png' class="rounded-circle hover ma-5"  @click="menu = !menu"></v-img>
          <v-container class="" @click="menu = !menu">
            <h1 class="text-h3 text-decoration-underline text-center my-10">Menu</h1>
            <v-list >            
              <v-list-item
                v-for="(link, i) in links"
                :key="i"
                active-color="primary"
                variant="plain"
                router :to="link.route"
                >
                <v-list-item-avatar>
                  <v-icon >{{link.icon}}</v-icon>
                </v-list-item-avatar>
                <v-list-item-title v-text="link.text" ></v-list-item-title>
              </v-list-item>
            </v-list>
          </v-container>
          
        </v-navigation-drawer>     
    </nav>
    
</template>
<script>


export default {
    data(){
        return{
            menu: false,
            links:[
                {icon: 'mdi-home', text: 'Home', route: '/'},
                {icon: 'mdi-account-tie', text: 'About Bubbas', route: '/about'},
                {icon: 'mdi-briefcase-outline', text: 'Our Work', route: '/work'},
                {icon: 'mdi-account-box', text: 'Contact Us', route: '/contact'},
                {icon: 'mdi-ballot', text: 'Get a Quote', route: '/quote'},
            ]
        }
    }
}
</script>
<style scoped>
.hover:hover{
  cursor: pointer;
}
@media only screen and (max-width: 600px) {
 .under{
  font-size: 1.75rem;
}
.under-1{
  font-size: 1.25rem;
}
}
@media only screen and (max-width: 1500px) {

}
@media only screen and (min-width: 600px) {
.under{
  font-size: 3rem;
}
.under-1{
  font-size: 2.125rem;
}
}
</style>

