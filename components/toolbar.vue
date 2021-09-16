<template>
    <v-toolbar flat class="secondary">
        <v-container class="mx-auto">
          <v-row class="justify-center">
            <a href="#profil">
              <v-btn text class="mx-4 black--text font-weight-bold text-subtitle-1">Profil</v-btn>
            </a>
            <a href="#work">
              <v-btn text class="mx-4 black--text font-weight-bold text-subtitle-1">Expériences Pro</v-btn>
            </a>
            <a href="#formation">
              <v-btn text class="mx-4 black--text font-weight-bold text-subtitle-1">Formation</v-btn>
            </a>
            <a @click="scroll(id)">
              <v-btn text class="mx-4 black--text font-weight-bold text-subtitle-1">Projets</v-btn>
            </a>
            <a href="#contact">
              <v-btn text class="mx-4 black--text font-weight-bold text-subtitle-1">Coordonnées</v-btn>
            </a>
          </v-row>
        </v-container>
      </v-toolbar>
</template>

<script>
  export default {
    name: 'Toolbar',

    methods: {
        scroll(id) {  
          console.log(id);
          document.getElementById(id).scrollIntoView({
          behavior: "smooth"
        });
      }
    }
  }
</script>