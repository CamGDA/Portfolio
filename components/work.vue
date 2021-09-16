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
                <v-col class="primary--text font-weight-medium"> {{ work.date }} </v-col>
              </v-row>
            </v-expansion-panel-header>
        
          <v-expansion-panel-content class="py-5"> {{ work.description }} </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
  </v-card>
</template>

<script>
  export default {
    name: 'Work',
    
    data: () => ({
      works: [
        {company: 'WeProov', job: 'Développement front-end | Stagiaire', date: 'Juillet 2021 - Août 2021 | Paris', description: "Stage d'observation. Vue.js, Nuxt.js, Vuetify, Bulma, Buefy, agilité, pair programming."},
        {company: 'MEDEF Essonne', job: 'Chargée de communication - Community Manager | Alternance', date: 'Septembre 2018 - Octobre 2020 | Évry', description: "Animation et développement des communautés, organisation d'événements entreprise et création de supports de communication."},
        {company: 'Pure Pommette', job: 'Stagiaire responsable vente', date: 'Avril 2017 - Juin 2017 | Québec, Vaudreuil-Dorion', description: "Vente au public, animation des réseaux sociaux et organisation d'un stand au salon 'Paternité, maternité et enfants' de Montréal."},
        {company: "L'Oréal ", job: "Stagiaire comptable puis job d'été", date: 'Mai 2016 - Août 2016 | Paris', description: "Contacts fournisseurs, saisie de factures sur le logiciel SAP et emailing"},
      ],
      items: [
        'default',
        'absolute',
        'fixed',
      ],
    }),
  }
</script>