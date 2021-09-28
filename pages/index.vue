<template>
  <v-app>
    <header>
      <Toolbar></Toolbar>
    </header>

    <!-- Sizes your content based upon application components -->
    <v-main class="lighten1">
      <!-- Provides the application the proper gutter -->

      <v-container class="pt-0" fluid>
        <Home></Home>
        <Profil></Profil>
        <Work></Work>
        <v-row>
          <v-col class="col-lg-6 col-sm-12">
            <Formation></Formation>
          </v-col>
          <v-col class="col-lg-6 col-sm-12">
            <Skills></Skills>
          </v-col>
        </v-row>
        <Project></Project>
        <Contact></Contact>
      </v-container>
    </v-main>
    <v-footer app>
      <v-col class="text-center" cols="12">
        {{ new Date().getFullYear() }} — <strong>Camille Gomes</strong>
      </v-col>
    </v-footer>
  </v-app>
</template>

<script>
import Home from '~/components/home.vue'
import Toolbar from '~/components/toolbar.vue'
import Profil from '~/components/profil.vue'
import Work from '~/components/work.vue'
import Formation from '~/components/formation.vue'
import Skills from '~/components/skills.vue'
import Project from '~/components/project.vue'
import Contact from '~/components/contact.vue'

export default {
  components: {
    Home,
    Toolbar,
    Profil,
    Work,
    Formation,
    Skills,
    Project,
    Contact,
  },
}
</script>
