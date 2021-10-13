<template>
  <v-card
    id="formation"
    elevation="1"
    class="mr-15 pa-3"
    color="lighten2"
    height="100%"
  >
    <v-card-title class="text-h4 font-weight-bold darken1--text pb-6"
      >Compétences
    </v-card-title>
    <v-card-text>
      <div v-for="(skill, i) in skills" :key="i">
        <div class="mb-3 darken1--text text-subtitle-1 font-weight-bold">
          {{ skill.language }}
        </div>
        <v-progress-linear
          :color="skill.color"
          height="10"
          :value="skill.value"
        ></v-progress-linear>
        <br />
      </div>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  name: 'Skills',

  data: () => ({
    skills: [
      {
        language: 'HTML / CSS',
        color: 'primary',
        value: '80',
      },
      {
        language: 'Javascript',
        color: 'indigo',
        value: '50',
      },
      {
        language: 'PHP',
        color: 'green',
        value: '40',
      },
      {
        language: 'Wordpress',
        color: 'blue',
        value: '50',
      },
      {
        language: 'Vue.js',
        color: 'red',
        value: '40',
      },
      {
        language: 'React',
        color: 'purple',
        value: '40',
      },
      {
        language: 'Bootstrap',
        color: 'orange',
        value: '40',
      },
    ],
  }),
}
</script>
