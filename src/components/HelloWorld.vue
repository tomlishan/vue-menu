<template>
  <div style="background-color:#F5F5F5;">

    
    <b-navbar toggleable="lg" variant="light">
      <b-navbar-brand href="#" class="col-md-1" >
          <b-img     
            height="40vh"
            width="70vw"
            :src="require('../assets/chinalifelogo.png')" />

          </b-navbar-brand>

      <b-navbar-brand href="#" class="col-md-1">iAgent</b-navbar-brand>
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <!-- <b-nav-item href="#">iAgent</b-nav-item>-->

        </b-navbar-nav>

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">

       <v-list-item class="grey lighten-3">  
        <v-list-item-avatar>
          <v-img src="https://randomuser.me/api/portraits/men/78.jpg"></v-img>
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title >hi abc</v-list-item-title>
          <v-list-item-subtitle>業務主任</v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

        </b-navbar-nav>
      </b-collapse>
    </b-navbar>

   <SideBarVuetify />

  </div>
</template>

<script>

import SideBarVuetify from './SideBarVuetify';
export default {
  data:{
    drawer:null
  },
  name: '',
  props: {
    msg: String
  },
  components: {
    SideBarVuetify
  },

}
</script>

<style scoped>
</style>
