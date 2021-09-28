<template>
  <div
    id="contact"
    elevation="1"
    class="my-8 pa-3"
    color="lighten2"
    height="600px"
  >
    <v-card color="black" height="260" width="500px" class="contact">
      <v-card-title class="white--text">thtrfh</v-card-title>
      <v-card-content class="white--text">blblblbl</v-card-content>
    </v-card>
    <div class="shape-container">
      <div class="shape"></div>
    </div>
    <!--<v-row class="ml-10">
      <v-col class="col-md-6">
        <v-img
          lazy-src="https://yannjarno.com/wp-content/uploads/2015/11/comment-devenir-developpeur-web-freelance.jpg"
          max-width="600"
          src="https://yannjarno.com/wp-content/uploads/2015/11/comment-devenir-developpeur-web-freelance.jpg"
        ></v-img>
      </v-col>
      <v-col class="d-flex align-center col-md-5 ml-md-auto">
        <v-card color="black" height="260" width="500px">
          <v-card-title class="white--text">thtrfh</v-card-title>
          <v-card-content class="white--text">blblblbl</v-card-content>
        </v-card>
      </v-col>
    </v-row> -->
  </div>
</template>

<script>
export default {
  name: 'Contact',
}
</script>

<style>
.shape-container {
  position: absolute;
  width: 100%;
  height: 330px;
  overflow: hidden;
  bottom: 3px;
}

.shape {
  position: relative;
  background-image: url(https://yannjarno.com/wp-content/uploads/2015/11/comment-devenir-developpeur-web-freelance.jpg);
  width: 3000px;
  height: 530px;
  border-radius: 50%;
}

.contact {
  left: calc(50vw - 600px);
}
</style>
