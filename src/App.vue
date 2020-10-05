<template>
  <v-app>
    <navBar/>
    <v-content class="mx-5 my-4">
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
import navBar from './components/navbar';

export default {
  name: 'App',

  components: {
    navBar,
  },

  data: () => ({
    //
  }),
};
</script>
