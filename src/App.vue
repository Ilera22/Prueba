<template>
  <v-app light>
    <v-toolbar color="light-blue lighten-1" dark fixed app>
      <v-toolbar-title>TodoWildrift</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn flat>Tier list</v-btn>
        <v-btn flat>Campeones</v-btn>
        <v-btn flat>Objetos</v-btn>
      </v-toolbar-items>
      <v-menu class="hidden-md-and-up">
        <v-toolbar-side-icon slot="activator"></v-toolbar-side-icon>

        <v-list>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>Tier List</v-list-item-title>
            </v-list-item-content>
          </v-list-item>

          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>Campeones</v-list-item-title>
            </v-list-item-content>
          </v-list-item>

          <v-list-item>
            <v-list-item-content>
              <v-list-item-title>Objetos</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-toolbar>

    <!-- Navigation bar ends 
    <v-toolbar class="light-blue accent-3">
      <v-toolbar-side-icon>
        <img src="assets/Logo.png" height="20px" />
      </v-toolbar-side-icon>
      <v-toolbar-title>TodoWildrift</v-toolbar-title>

      <v-spacer></v-spacer>
      <v-toolbar-items>
        <v-btn flat>Tier list</v-btn>
        <v-btn flat>Campeones</v-btn>
        <v-btn flat>Objetos</v-btn>
      </v-toolbar-items>
    </v-toolbar>-->

    <v-content>
      <section>
        <v-parallax :src="imageLink.sub_main" height="600">
          <v-layout column align-center justify-center class="white--text">
            <h1
              class="white--text mb-2 display-1 text-xs-center"
              style="font-weight: 900; text-shadow: 3px 2px #000000"
            >
              Bienvenidos a TodoWildrift
            </h1>
            <div
              class="white--text subheading mb-3 text-xs-center"
              style="font-weight: 900; text-shadow: 2px 2px #000000"
            >
              Tu referente de informacion de Wildrift
            </div>
          </v-layout>
        </v-parallax>
      </section>

      <section>
        <v-layout column wrap class="my-5" align-center>
          <v-flex xs12 sm4 class="my-3">
            <div class="text-xs-center">
              <h2 class="headline">Tier List</h2>
              <span class="subheading"> Pronto tendremos mas </span>
            </div>
          </v-flex>
        </v-layout>
      </section>

      <section></section>
      ----------------------------------------------------------

      <v-footer dark padless>
        <v-card class="flex" flat tile>
          <v-card-title class="light-blue lighten-1">
            <strong class="heading">Siguenos en Nuestras Redes </strong>

            <v-spacer></v-spacer>

            <v-btn
              color="none"
              elevation="2"
              icon
              href="https://www.youtube.com"
            >
              <v-icon color="white"> fab fa-facebook-f </v-icon>
            </v-btn>

            <v-btn
              color="none"
              elevation="2"
              icon
              href="https://www.youtube.com"
            >
              <v-icon color="white"> fab fa-twitter </v-icon>
            </v-btn>

            <v-btn
              color="none"
              elevation="2"
              icon
              href="https://www.youtube.com"
            >
              <v-icon color="white"> fab fa-reddit-alien </v-icon>
            </v-btn>

            <v-btn
              color="none"
              elevation="2"
              icon
              href="https://www.youtube.com"
            >
              <v-icon color="white"> fab fa-instagram </v-icon>
            </v-btn>

            <v-btn
              color="none"
              elevation="2"
              icon
              href="https://www.youtube.com"
            >
              <v-icon color="white"> fab fa-discord </v-icon>
            </v-btn>

            <v-btn v-for="icon in icons" :key="icon" class="mx-4" dark icon>
              <v-icon size="24px">
                {{ icon }}
              </v-icon>
            </v-btn>
          </v-card-title>

          <v-card-text class="py-2 white--text text-center">
            {{ new Date().getFullYear() }} — <strong>Ilera</strong>
          </v-card-text>
        </v-card>
      </v-footer>
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data: function () {
    return {
      imageLink: {
        main:
          "https://firebasestorage.googleapis.com/v0/b/endorfinevue.appspot.com/o/assets%2Fb13f0434-b228-11e6-8e5d-5252025056ab_web_scale_0.4666667_0.4666667__.jpg?alt=media&token=660df23e-599e-434b-9313-ba69c973eeea",
        sub_main: "https://wallpaperaccess.com/full/3130430.jpg",
        logo:
          "https://drive.google.com/file/d/1MCiAXhxLDEpsyTJy6jzySnr8TctIHcxx/view?usp=sharing",
        social_cover: "https://wallpaperaccess.com/thumb/1935362.jpg",
      },
    };
  },

  computed: {
    imgHeight: function () {
      var offset = 320;
      console.log("new image height is " + (this.pageHeight - offset));
      return this.pageHeight - offset;
    },
  },
};
</script>


<style>
</style>
