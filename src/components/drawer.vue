<template>
  <v-navigation-drawer
    app
    v-model="drawer"
    dark
    class="deep-purple"
    src="https://cdn.vuetifyjs.com/images/backgrounds/bg-2.jpg"
    :mini-variant.sync="mini"
  >
    <!-- width="22%" expand-on-hover="" -->
    <v-list>
      <v-list-item class="px-2 justify-center">
        <v-list-item-avatar size="50">
          <v-img src="https://randomuser.me/api/portraits/women/85.jpg"></v-img>
        </v-list-item-avatar>
      </v-list-item>

      <v-list-item link class="justify-center">
        <v-list-item-content>
          <v-list-item-title class="title">Sandra Adams</v-list-item-title>
          <v-list-item-subtitle>sandra_a88@gmail.com</v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>
    </v-list>

    <v-divider></v-divider>

    <v-list nav dense>
      <v-list-item-group v-model="group">
        <!-- //active-class="deep-purple--text text--accent-4"  -->
        <v-list-item v-for="link in links" v-bind:key="link.text" router :to="link.route">
          <v-list-tile-action>
            <v-icon middle color="white--text" left>{{link.icon}}</v-icon>
          </v-list-tile-action>
          <v-list-content>
            <v-list-item-title>{{link.text}}</v-list-item-title>
          </v-list-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
export default {
  data() {
    return {
      drawer: true,
      mini: true,
      links: [
        { icon: "mdi-view-dashboard", text: "Dashboard", route: "/" },
        { icon: "mdi-folder", text: "My Projects", route: "/projects" },
        { icon: "mdi-thumb-up", text: "Team", route: "/team" }
      ]
    };
  }
};
</script>