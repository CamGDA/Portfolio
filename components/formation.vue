<template>
  <v-card id="formation" elevation="1" max-width="600" class="mx-15 my-8 pa-3" color="lighten2">
    <v-card-title class="text-h4 font-weight-bold darken1--text pb-6">Formations</v-card-title>

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
              <row class="d-md-flex">
                <v-col cols="10">
                  <div class="font-weight-bold darken1--text">
                    {{ formation.year }}<strong> @{{ formation.institute }}</strong>
                  </div>
                  <div>{{ formation.description }}</div>
                </v-col>
                <v-col cols="2">
                  <v-avatar>
                    <v-img
                      :src="formation.logo"
                    ></v-img>
                  </v-avatar>
                </v-col>
              </row>
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
          logo: "https://enpantoufles.com/uploads/companies/1560256962_Picto%20noir%20+%20vert%201667x1667.png"
        },
        {
          color: 'amber', 
          year: '2021',
          institute: 'Université Gustave Eiffel ',
          description: 'DU Développeur Web, Webdesigner',
          logo: "https://i.ytimg.com/vi/86Ltu9w-5jY/maxresdefault.jpg"
        },
        {
          color: 'orange',
          year: '2018 - 2020',
          institute: 'Sup de Pub | Groupe INSEEC ',
          description: 'Master Événementiel et Communication Culturelle ',
          logo: "https://www.akumaw.com/wp-content/uploads/2020/07/logo-sup-de-pub-190524023751.png"
        },
        {
          color: 'cyan', 
          year: '2017 - 2018',
          institute: "Université d'Evry Val d'Essonne",
          description: 'Licence Professionnelle Chargé de Communication',
          logo: "https://upload.wikimedia.org/wikipedia/en/5/55/University_of_%C3%89vry_Val_d%27Essonne_%28logo%29.png"
        },
        {
          color: 'green',
          year: '2015 - 2017',
          institute: "Université d'Evry Val d'Essonne",
          description: 'DUT Gestion des Entreprises et des Administrations',
          logo: "https://upload.wikimedia.org/wikipedia/en/5/55/University_of_%C3%89vry_Val_d%27Essonne_%28logo%29.png"
        },
      ],
    }),
  }

</script>