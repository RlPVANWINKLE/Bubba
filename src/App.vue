<template>
  <v-app>
    <nav-bar></nav-bar>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import NavBar from './components/NavBar.vue'
export default {
  name: 'App',
  components:{
    NavBar,
  }
};
</script>
<style >
body{
  font-family: 'Chivo', sans-serif;
  font-family: 'Lato', sans-serif;
  font-family: 'Lobster', cursive;
}
</style>

