<template>
  <div class="home">
    <drawer />
    <h1 class="subheading grey--text">Project</h1>

    <v-container class="my-2">
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Alias eius assumenda quisquam distinctio a, magnam nulla amet saepe voluptatem impedit rerum odio dicta dolores, sequi pariatur. Accusamus similique exercitationem vel?</p>
      <v-btn outlined color="primary">Roba_G</v-btn>
      <v-btn outlined rounded>
        <v-icon left>mdi-email</v-icon>Roba_G
      </v-btn>
    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src
import drawer from "../../components/drawer.vue";

export default {
  components: {
    drawer
  }
};
</script>
