<template>
  <v-card id="formation" elevation="1" max-width="600" class="justify-center mx-15 my-8 pa-3" color="lighten2">
    <v-card-title class="text-h4 font-weight-bold darken1--text pb-6">Formations</v-card-title>

  <!--<div>
      <v-card width="700px" class="pa-5 d-flex justify-space-around ">
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
      </v-card>
    </div>-->

    <v-timeline
            align-top
            dense
          >
            <v-timeline-item
              v-for="(formation, i) in formations"
            :key="i"
            :color="formation.color"
              small
            >
              <div>
                <div class="font-weight-normal">
                  <strong>{{ formation.year }}</strong> @{{ formation.institute }}
                </div>
                <div>{{ formation.description }}</div>
              </div>
            </v-timeline-item>
          </v-timeline>

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
        {/* amber */
          color: 'amber', 
          year: '2021',
          institute: 'Université Gustave Eiffel ',
          description: 'DU Développeur Web, Webdesigner',
        },
        {
          color: 'orange', /* orange */
          year: '2018 - 2020',
          institute: 'Sup de Pub | Groupe INSEEC ',
          description: 'Master Événementiel et Communication Culturelle ',
        },
        {
          color: 'cyan', /* cyan */
          year: '2017 - 2018',
          institute: "Université d'Evry Val d'Essonne",
          description: 'Licence Professionnelle Chargé de Communication',
        },
        {
          color: 'green',
          year: '2015 - 2017',
          institute: "Université d'Evry Val d'Essonne",
          description: 'DUT Gestion des Entreprises et des Administrations',
        },
      ],
    }),
  }

</script>