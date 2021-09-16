<template>
  <v-card id="profil" elevation="1" class="mx-15 my-8 pa-3" color="lighten2">

    <div class="d-flex">
      <v-col cols="8">
        <v-card-title class="text-h4 font-weight-bold darken1--text pb-6">Mon profil</v-card-title>
        <v-card-text class="darken1--text text-subtitle-1 text-justify">
          <div>Bonjour !</div>
          <br/>
          <div>Souhaitant aujourd’hui m’orienter vers le métier de <strong class="darken1--text">développeur web</strong>, je suis à la recherche d'un 
          <strong class="darken1--text">contrat d'apprentissage.</strong></div>
          <v-divider inset></v-divider>
          <div>Durant mes deux dernières années d’études en alternance en tant que chargée de communication, j’ai eu l’occasion de participer à la création d’un site 
            internet. Pendant cette expérience, j’ai eu l’opportunité de découvrir le langage HTML ce qui m’a donné envie d’en apprendre plus sur les différents 
            langages de développement. J'ai d'abord réalisé un diplôme  universitaire : Développeur web, webdesigner à l’Université Gustave Eiffel où j’ai eu l’occasion 
            d’apprendre Javascript et PHP et de me perfectionner en HTML et CSS. Je suis aujourd'hui inscrite à la <a href="https://drive.google.com/file/d/1Uswf0nChaBfRU6gfVYJfMmW5Yug23dLi/view?usp=sharing">
            formation en alternance O'Clock </a> : concepteur développeur d'applications.
          </div>
        </v-card-text>
      </v-col>
      <v-col cols="4">
        <v-card class="pa-5 mr-5" height="100%">
          <v-row class="d-flex flex-column">
             <v-col  class="d-flex justify-center">
              <v-avatar size="164">
                <img
                  src="~/assets/images/profil.jpg"
                >
              </v-avatar>
            </v-col>
            <v-col>
              <v-card-title class="primary--text ml-5 pa-0 font-weight-bold">Camille Gomes de Assunçao</v-card-title>
            </v-col>
            <v-col>
              <v-card-subtitle class="primary--text ml-5 pa-0 font-weight-bold">Apprentie développeur web d'application</v-card-subtitle>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </div>

  </v-card>
</template>

<script>
  export default {
    name: 'Profil',
    
  }
</script>