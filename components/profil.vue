<template>
  <v-card id="profil" elevation="1" class="mx-15 my-8 pa-3" color="lighten2">
    <div id="responsive" class="d-flex">
      <v-col class="col-lg-8 col-sm-12">
        <v-card-title class="text-h4 font-weight-bold darken1--text pb-6">Mon profil</v-card-title>
        <v-card-text class="center darken1--text text-subtitle-1 text-justify">
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
      <v-col class="col-lg-4 col-sm-12">
        <v-card class="pa-5 mr-5" height="100%">
          <v-row class="d-flex flex-column">
            <v-col class="d-flex justify-center">
                <v-avatar slot="offset" class="mx-auto d-block" size="150">
                  <img contain src="~/assets/images/profil.jpg" alt="Avatar">
                </v-avatar>
              </v-col>
              <v-col class="pb-0">
                <v-card-text class="darken1--text">
                  <div class="text-center">
                    <h3 class="font-weight-bold primary--text mb-1">Camille Gomes de Assunçao</h3>
                    <div class="body-1 mb-3 ">Apprentie développeur web d'application</div>
                    <div class="mb-2">95 Avenue de la République, 91230, Montgeron</div>
                    <div class="mb-2">camillegomes91@gmail.com</div>
                    <div class="mb-2">06 01 30 72 88</div>
                  </div>
                </v-card-text>
              </v-col>
              <v-col class="pa-0">
                <v-card-actions class="white justify-center">
                  <v-btn
                    v-for="(social, i) in socials"
                    :key="i"
                    :color="social.color"
                    class="white--text"
                    fab
                    icon
                    small
                  >
                    <v-icon>{{ social.icon }}</v-icon>
                  </v-btn>
                </v-card-actions>
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

    data: () => ({
      socials: [
        {
          icon: 'mdi-facebook',
          color: 'indigo',
        },
        {
          icon: 'mdi-github',
          color: 'black lighten-3',
        },
        {
          icon: 'mdi-email',
          color: 'cyan darken-1',
        },
      
      ],
    }),
  }
</script>

<style scoped>

@media screen and (max-width: 1280px)
{
    #responsive {
      flex-direction: column;
    }

}
</style>