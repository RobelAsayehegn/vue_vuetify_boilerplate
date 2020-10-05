<template>
  <div class="home">
    <drawer />
    <h1 class="subheading grey--text">DashBoard</h1>
    <v-container class="my-2">
      <!-- fluid="true" -->
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Alias eius assumenda quisquam distinctio a, magnam nulla amet saepe voluptatem impedit rerum odio dicta dolores, sequi pariatur. Accusamus similique exercitationem vel?</p>
      <v-btn outlined>Roba_G</v-btn>
      <v-btn outlined rounded>
        <v-icon left>mdi-email</v-icon>Roba_G
      </v-btn>
    </v-container>

    <v-expansion-panels popout inset focusable flat hover tile>
      <v-expansion-panel v-for="(item,i) in 5" :key="i">
        <v-expansion-panel-header>Item</v-expansion-panel-header>
        <v-expansion-panel-content>
          <v-layout>
            <v-list-item-avatar size="50">
              <v-img src="https://randomuser.me/api/portraits/women/85.jpg"></v-img>
            </v-list-item-avatar>
            <v-icon>mdi-email</v-icon>
          </v-layout>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-expansion-panels>
    <!-- /////////////////////////////////////////// -->
    <v-card class="mx-auto" max-width="400" shaped>
      <v-list-item class="px-2 justify-center">
        <v-list-item-avatar size="100">
          <v-img src="https://randomuser.me/api/portraits/men/85.jpg"></v-img>
        </v-list-item-avatar>
      </v-list-item>

      <v-card-title>Dr Abebe Hailu</v-card-title>

      <v-card-subtitle class="pb-0">Number 10</v-card-subtitle>

      <v-card-text class="text--primary">
        <div>Whitehaven Beach</div>

        <div>Whitsunday Island, Whitsunday Islands</div>
      </v-card-text>

      <v-card-actions>
        <v-btn color="orange" text>Share</v-btn>

        <v-btn color="orange" text>Explore</v-btn>
      </v-card-actions>
    </v-card>
    <!-- ////////////////////////////////////////////////// -->
    <v-row>
      <v-col cols="11" sm="5">
        <v-menu
          ref="menu"
          v-model="menu2"
          :close-on-content-click="false"
          :nudge-right="40"
          :return-value.sync="time"
          transition="scale-transition"
          offset-y
          max-width="290px"
          min-width="290px"
        >
          <template v-slot:activator="{ on, attrs }">
            <v-text-field
              v-model="time"
              label="Picker in menu"
              prepend-icon="mdi-clock"
              readonly
              v-bind="attrs"
              v-on="on"
            ></v-text-field>
          </template>
          <v-time-picker
            v-if="menu2"
            v-model="time"
            full-width
            @click:minute="$refs.menu.save(time)"
          ></v-time-picker>
        </v-menu>
      </v-col>
      <v-spacer></v-spacer>
      <v-col cols="11" sm="5">
        <v-dialog ref="dialog" v-model="modal2" :return-value.sync="time" persistent width="290px">
          <template v-slot:activator="{ on, attrs }">
            <v-text-field
              v-model="time"
              label="Picker in dialog"
              prepend-icon="mdi-clock"
              readonly
              v-bind="attrs"
              v-on="on"
            ></v-text-field>
          </template>
          <v-time-picker v-if="modal2" v-model="time" full-width>
            <v-spacer></v-spacer>
            <v-btn text color="primary" @click="modal2 = false">Cancel</v-btn>
            <v-btn text color="primary" @click="$refs.dialog.save(time)">OK</v-btn>
          </v-time-picker>
        </v-dialog>
      </v-col>
    </v-row>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import drawer from "../../components/drawer.vue";
// import drawer from "../components/drawer";

export default {
  // name:Dashboard,
  data() {
    return {
      time: null,
      menu2: false,
      modal2: false,
    };
  },
  components: {
    drawer,
  },
};
</script>
