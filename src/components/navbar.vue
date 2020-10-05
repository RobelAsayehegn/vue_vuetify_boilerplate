<template>
  <nav>
    <v-app-bar app flat class="gray--text">
      <v-app-bar-nav-icon @click.stop="mini = !mini"></v-app-bar-nav-icon>

      <v-toolbar-title class="text-uppercase">
        <span class="font-weight-light">Smart</span>
        <span>Med</span>
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn @click="drawer = !drawer" text>
        <span class="mr-2">Latest Release</span>
        <!-- <v-icon>mdi-open-in-new</v-icon> -->
      </v-btn>
    </v-app-bar>
    <!-- ///////////////navigation///////////////// -->
  </nav>
</template>

<script>
export default {
  // data(){
  //     return{
  //         drawer : true,
  //         mini: true,
  //         links: [
  //             { icon: 'mdi-view-dashboard', text: 'Dashboard', route: '/' },
  //             { icon: 'mdi-folder', text: 'My Projects', route: '/projects' },
  //             { icon: 'mdi-thumb-up', text: 'Team', route: '/team' },
  //         ],
  //     }
  // }
};
</script>