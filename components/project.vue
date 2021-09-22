<template>
    <v-card id="project" elevation="1" class="mx-15 my-8 pa-3" color="lighten2">
      <v-card-title class="text-h4 font-weight-bold darken1--text pb-6">Projets</v-card-title>
      <div class="d-flex flex-wrap justify-space-between">
        <v-card
          v-for="(project,i) in projects"
          :key="i"
          class="ma-5"
          max-width="344"
          outlined
        >
          <v-list-item three-line>
            <v-list-item-content>
              <div class="text-overline mb-4">
                {{ project.slide }}
              </div>
              <v-list-item-title class="text-h5 mb-1">
                {{ project.title }}
              </v-list-item-title>
              <v-list-item-subtitle>{{ project.subtitle }}</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>

          <div>
            <v-chip
              class="ma-2 ml-4"
              color="blue"
              text-color="white"
              small
            >
              {{ project.chip1 }}
            </v-chip>

            <v-chip
              class="ma-2"
              color="blue"
              text-color="white"
              small
            >
             {{ project.chip2 }}
            </v-chip>

            <v-chip
              class="ma-2"
              color="blue"
              text-color="white"
              small
            >
              {{ project.chip3 }}
            </v-chip>

            <v-chip
              class="ma-2"
              color="blue"
              text-color="white"
              small
            >
              {{ project.chip4 }}
            </v-chip>
          </div>

          <v-card-actions>
            <a :href="project.src">
              <v-btn
                outlined
                rounded
                text
              >
              <v-icon class="mr-2">mdi-github</v-icon>
                Voir le projet
              </v-btn>
            </a>
          </v-card-actions>
        </v-card>
      </div>
    </v-card>
  
</template>

<script>

  export default {
    name: 'Project',

    data: () => ({
      projects: [
        {
          slide: 'PROJET 1',
          title: 'To Do List Nuxt',
          subtitle: 'Simple To Do List avec ajout, modification et suppression de tâches.',
          src: "https://github.com/CamGDA/TodoListNuxt",
          chip1: 'Nuxt',
          chip2: 'Vue',
          chip3: 'JS',
          chip4: "Vuetify",
        },
        {
            slide: 'PROJET 2',
            title: 'Epicerie en ligne',
            subtitle: "Site e-commerce en PHP avec inscription, connexion, modification d'un profil et panier",
            src: "https://github.com/CamGDA/Epicerie-en-ligne",
            chip1: 'PHP',
            chip2: 'Bootstrap',
            chip3: 'MySQL',
          },
          {
          slide: 'PROJET 3',
          title: 'Portfolio',
          subtitle: 'Portfolio responsive',
          src: "https://github.com/CamGDA/portfolio",
          chip1: 'Nuxt',
          chip2: 'Vue',
          chip3: 'JS',
          chip4: "Vuetify"
        },
      ],
      model: 0,
    }),
    
  }

</script>
