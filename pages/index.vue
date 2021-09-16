<template>
  <v-app>
    <header>
      <Toolbar></Toolbar>
    </header>

    <!-- Sizes your content based upon application components -->
    <v-main class="lighten1">
      <!-- Provides the application the proper gutter -->

        <v-container class="pt-0" fluid>
          <v-img src="https://images.unsplash.com/photo-1457612928689-a1ab27da0dad?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1050&q=80" height="570">
            <Profil></Profil>
          </v-img>
          <Work></Work>
          <v-img src="https://images.unsplash.com/photo-1579403124614-197f69d8187b?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=700&q=80" height="">
          <Formation></Formation>
        </v-img>
        </v-container>
    
    </v-main>

    <v-footer app>
      <v-col
        class="text-center"
        cols="12"
      >
        {{ new Date().getFullYear() }} — <strong>Camille Gomes</strong>
      </v-col>
    </v-footer>
  </v-app>
</template>

<script>

import Toolbar from "~/components/toolbar.vue";
import Profil from "~/components/profil.vue";
import Work from "~/components/work.vue";
import Formation from "~/components/formation.vue";

  export default {
    components: { Toolbar, Profil, Work, Formation },

  }
</script>


