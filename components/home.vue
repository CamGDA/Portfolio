<template>
    <v-img
    src="https://espritweb.fr/wp-content/uploads/2020/04/image-mise-en-avant-pourquoi-devenir-developpeur-web-1692x846.png"
    gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
    height="600px"
    class="d-flex align-end"
    >
    <v-card-title class="font-weight-medium white--text text-lg-h1 text-md-h2 text-xs-h2">
        Mon Portfolio
    </v-card-title>
    </v-img>
</template>

<script>

export default ({
    name: 'Home',
})
</script>

<style scoped>


@media screen and (max-width: 1280px)
{
    v-card-title {
      flex-direction: column;
    }

}

</style>