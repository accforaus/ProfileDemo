<template>
  <v-app>
    <v-app-bar
      app
      color="transparent"
      light
      flat
      hide-on-scroll
    >
      <v-toolbar-title class="headline font-weight-light">Profile</v-toolbar-title>
      <v-spacer></v-spacer>
    </v-app-bar>
    <v-content>
      <HelloWorld/>
    </v-content>
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
    //
  }),
};
</script>
