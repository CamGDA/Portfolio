<template>
    <v-toolbar color="secondary" fixed app>
      <v-col class="d-flex justify-start align-center">
        <v-icon color="black">mdi-flower</v-icon>
        <v-toolbar-title class="mx-4 black--text"><strong>Camille</strong> GOMES</v-toolbar-title>
      </v-col>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn v-for="(item, i) in menu" :key="i" :to="item.link" color="black" text>{{
          item.title
        }}</v-btn>
      </v-toolbar-items>
      <v-menu class="hidden-md-and-up" 
        :offset-y="true"
        close-on-content-click>
          <template v-slot:activator="{ on, attrs }">
            <v-app-bar-nav-icon 
              v-on="on" 
              v-bind="attrs"
              class="hidden-md-and-up">
            </v-app-bar-nav-icon>
          </template>
          <v-list class="d-flex flex-column pa-5 hidden-md-and-up">
            <v-list-tile v-for="(item, i) in menu" :key="i" :to="item.link" class="mb-3">
              <v-list-tile-content>
                <v-list-tile-title>{{ item.title }}</v-list-tile-title>
              </v-list-tile-content>
            </v-list-tile>
          </v-list>
        </v-menu>
      
    </v-toolbar>
  
</template>

<script>

  export default {
    name: 'Toolbar',

    data() {
      return {
        menu: [
          { title: "Profil", link: "#profil" },
          { title: "Expériences Pro", link: "#work"},
          { title: "Formation", link: "#formation" },
          { title: "Projets", link: "#project" },
          { title: "Coordonnées", link: "#contact" }
          ]
        }
      },

    methods: {
    menuItems() {
      return this.menu;
    }

      }
  }
</script>

