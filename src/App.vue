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
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    collapseOnScroll: true,
  }),
};
</script>
