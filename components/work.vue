<template>
  <v-card id="work" elevation="1" class="mx-15 my-8 pa-3" color="lighten2">
    <v-card-title class="text-h4 font-weight-bold darken1--text pb-6">Expériences professionnelles</v-card-title>
      <v-expansion-panels focusable>
        <v-expansion-panel
          v-for="(work,i) in works"
          :key="i"
        >
            <v-expansion-panel-header > 
              <v-row class="justify-center">
                <v-col class="text-h6 font-weight-bold darken1--text"> {{ work.company }} </v-col>
                <v-col class="primary--text font-weight-medium d-flex align-center"> {{ work.date }} </v-col>
              </v-row>
            </v-expansion-panel-header>
      
          <v-expansion-panel-content class="py-5"> 
            <v-list-item three-line>
              <v-list-item-content>
                <div class="text-overline mb-4">
                  {{ work.job }}
                </div>
                <v-list-item-title class="text-h5 mb-4">
                  {{ work.title }}
                </v-list-item-title>
                <v-list-item-subtitle>{{ work.description }} </v-list-item-subtitle>
              </v-list-item-content>

              <v-list-item-avatar
                tile
                size="100"
              >
                <v-img :src="work.logo"></v-img>
              </v-list-item-avatar>
            </v-list-item>

          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
      
  </v-card>
</template>

<script>
  export default {
    name: 'Work',
    
    data: () => ({
      works: [
        {
          company: 'WeProov', 
          title: 'Développement front-end', 
          job: "Stagiaire", 
          date: 'Juillet 2021 - Août 2021 | Paris', 
          description: "Stage d'observation. Vue.js, Nuxt.js, Vuetify, Bulma, Buefy, agilité, pair programming.", 
          logo: "https://www.jaimelesstartups.fr/wp-content/uploads/2019/06/logo-weproov.png"
        },
        {
          company: 'MEDEF Essonne', 
          title: 'Chargée de communication - Community Manager', 
          job: "Alternance", date: 'Septembre 2018 - Octobre 2020 | Évry', 
          description: "Animation et développement des communautés, organisation d'événements entreprise et création de supports de communication.", 
          logo: "https://pbs.twimg.com/profile_images/1418217372758941698/7iyZaeK8.jpg"
        },
        {
          company: 'Pure Pommette', 
          title: 'Responsable vente', 
          job: "Stagiaire", 
          date: 'Avril 2017 - Juin 2017 | Québec, Vaudreuil-Dorion', 
          description: "Vente au public, animation des réseaux sociaux et organisation d'un stand au salon 'Paternité, maternité et enfants' de Montréal.", 
          logo: "https://s3-media0.fl.yelpcdn.com/bphoto/hh6ueT5Dr5G7Iv29NZuysA/l.jpg"
        },
        {
          company: "L'Oréal ", 
          title: "Comptable", 
          job: "Stagiaire", 
          date: 'Mai 2016 - Août 2016 | Paris', 
          description: "Contacts fournisseurs, saisie de factures sur le logiciel SAP et emailing", 
          logo: "https://fontmeme.com/images/loreal-logo-font.png"
        },
      ],
    }),
  }
</script>