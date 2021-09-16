<template>
  <v-card elevation="1" class="mx-15 my-8 pa-3" color="lighten2">
    <v-card-title class="text-h4 font-weight-bold darken1--text pb-6">Formations</v-card-title>

    <div width="700px">
      <v-timeline>
        <v-timeline-item
          v-for="(formation, i) in formations"
          :key="i"
          :color="formation.color"
          small
        >
          <template v-slot:opposite>
            <span
              :class="`headline font-weight-bold ${formation.color}--text`"
              v-text="formation.year"
            ></span>
          </template>
          <div class="py-4">
            <h2 :class="`headline font-weight-light mb-4 ${formation.color}--text`">
              {{ formation.institute }}
            </h2>
            <div>
              {{ formation.description }}
            </div>
          </div>
        </v-timeline-item>
      </v-timeline>
    </div>
  </v-card>
  
</template>

<script>

  export default {
    name: 'Formation',
     data: () => ({
      formations: [
        {
          color: 'pink',
          year: '2021 | 2023',
          institute: "Formation O'Clock",
          description: 'Concepteur développeur d’application',
        },
        {
          color: 'amber',
          year: '2021',
          institute: 'Université Gustave Eiffel ',
          description: 'DU Développeur Web, Webdesigner',
        },
        {
          color: 'orange',
          year: '2018 - 2020 | Paris',
          institute: 'Sup de Pub | Groupe INSEEC ',
          description: 'Master Événementiel et Communication Culturelle ',
        },
        {
          color: 'cyan',
          year: '2017 - 2018 | Évry',
          institute: "Université d'Evry Val d'Essonne",
          description: 'Licence Professionnelle Chargé de Communication',
        },
        {
          color: 'green',
          year: '2015 - 2017 | Évry',
          institute: "Université d'Evry Val d'Essonne",
          description: 'DUT Gestion des Entreprises et des Administrations',
        },
      ],
    }),
  }

</script>