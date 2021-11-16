<template>
  <div
    id="contact"
    elevation="1"
    class="my-8 pa-3"
    color="lighten2"
    height="600px"
  >
    <v-img
      src="https://yannjarno.com/wp-content/uploads/2015/11/comment-devenir-developpeur-web-freelance.jpg"
      gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
      height="500"
      class="d-flex align-center"
    >
      <div class="d-flex justify-center">
        <v-card color="rgb(232, 248, 245, 0.8)" height="280" width="700px">
          <v-card-title
            class="text-h4 font-weight-bold darken1--text pb-6 justify-center"
          >
            Coordonnées
          </v-card-title>
          <v-card-title class="darken1--text justify-center"
            >camillegomes91@gmail.com</v-card-title
          >
          <v-card-title class="darken1--text justify-center"
            >06 01 30 72 88</v-card-title
          >
          <v-card-actions class="justify-center">
            <v-btn
              v-for="(social, i) in socials"
              :key="i"
              :color="social.color"
              :href="social.link"
              class="white--text"
              fab
              icon
              small
            >
              <v-icon>{{ social.icon }}</v-icon>
            </v-btn>
          </v-card-actions>
        </v-card>
      </div>
    </v-img>
  </div>
</template>

<script>
export default {
  name: 'Contact',

  data: () => ({
    socials: [
      {
        icon: 'mdi-github',
        color: 'black lighten-3',
        link: 'https://github.com/Camille-Gomes',
      },
      {
        icon: 'mdi-linkedin',
        color: 'cyan darken-1',
        link: 'https://www.linkedin.com/in/camille-gomes-de-assun%C3%A7ao-34a106157/',
      },
    ],
  }),
}
</script>
