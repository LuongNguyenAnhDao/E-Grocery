<template>
    
    <v-footer style="background-color: black;" padless>
      <v-card flat tile style="background-color: black;" class="black text-white py-12 px-5" width="100%">
        <v-row>
          <v-col cols="12" xs="12" sm="6" md="4" class="pa-16">
            <v-toolbar color="transparent" flat>
              <v-badge color="#D5F0DB" dot>
                <v-img src="1.png" contain width="30"></v-img>
              </v-badge>
  
              <v-toolbar-title class="ml-4">
                <span class="text-green">e</span><strong>Grocery</strong>
              </v-toolbar-title>
            </v-toolbar>
            <v-card-text class="pt-0">
              <v-btn
                v-for="icon in icons"
                :key="icon"
                class="mx-1"
                icon
                fab
                outlined
                small
              >
                <v-icon size="20px">
                    {{ icon }}
                </v-icon>
              </v-btn>
            </v-card-text>
          </v-col>
          <v-col cols="12" xs="12" sm="6" md="2">
            <v-card-text class="text-white pt-0">
              <h3>About</h3>
            </v-card-text>
            <v-card-text class="text-grey"> How it Work</v-card-text>
            <v-card-text class="text-grey mt-n4"> Our Promrams </v-card-text>
            <v-card-text class="text-grey mt-n4"> Promotions </v-card-text>
            <v-card-text class="text-grey mt-n4"> Refer A Friend </v-card-text>
          </v-col>
          <v-col cols="12" xs="12" sm="6" md="2">
            <v-card-text class="text-white pt-0">
              <h3>Dellvery</h3>
            </v-card-text>
            <v-card-text class="text-grey"> Cost on Delevery </v-card-text>
            <v-card-text class="text-grey mt-n4"> Payment Method </v-card-text>
            <v-card-text class="text-grey mt-n4"> Delevery Astus </v-card-text>
            <v-card-text class="text-grey mt-n4"> Returns </v-card-text>
          </v-col>
          <v-col cols="12" xs="12" sm="6" md="4">
            <v-card-text class="text-white pt-0">
              <h3>Contact</h3>
            </v-card-text>
            <v-card-text class="text-grey"> THUY DU XINH DEP </v-card-text>
            <v-card-text class="text-grey mt-n4">
              216 / C EAST Road
            </v-card-text>
            <v-card-text class="text-grey mt-n4"> aae.idapro.com </v-card-text>
            <v-card-text class="text-grey mt-n4"> -B8254552214 </v-card-text>
          </v-col>
        </v-row>
      </v-card>
    </v-footer>
  </template>
  
  <script>
  export default {
    data: () => ({
      icons: [
        "fab fa-apple",
        "fab fa-google-plus-g",
        "fab fa-twitter",
        "fab fa-facebook-f",
      ],
    }),
  };
  </script>
  
  <style>
  </style>