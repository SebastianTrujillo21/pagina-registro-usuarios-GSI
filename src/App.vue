<template>
  <v-app>
    <v-app-bar color="blue" :collapse="!collapseOnScroll" :collapse-on-scroll="collapseOnScroll" absolute dark> 
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-toolbar-title>Marcador de asistencia GSI</v-toolbar-title>
      <v-spacer></v-spacer>   
      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>
    </v-app-bar>
    <v-main>
          <HelloWorld/>
          <!-- <LoginGSI/> -->
    </v-main>

  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
// import LoginGSI from './components/LoginGSI.vue';
export default {
  name: 'App',

  components: {
    HelloWorld,
    // LoginGSI
},

  data: () => ({
    collapseOnScroll: true,
  }),
};
</script>
