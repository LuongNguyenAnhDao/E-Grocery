<template>
  <v-app>
    <navbar/>
    <v-container fluid>
      <v-row>
        <v-col cols="12">
          <v-card class="mx-auto rounded-xl" flat>
            <v-img src="cover2.png"
             max-height="100%"
             max-width="100%"
             contain
             >
            <v-card-title class="top ml-10">
              <h2 class="title1">Order your</h2>
            </v-card-title>
            <v-card-title class="mt-n8 ml-10">
              <h2 class="title2">Daily Groceries</h2>
            </v-card-title>
            <v-card-text class="ml-10">
              <h3 class="text-green">#Free Delivery</h3>
            </v-card-text>
            <v-card-text class="ml-10">
              <v-row>
                <v-col cols="4">
                  <v-text-field
                      label="Search your daily groceries"
                      class="d-none d-sm-none d-md-flex"
                      prepend-inner-icon="mdi:mdi-magnify"
                      variant="solo outlined"
                      rounded
                    ></v-text-field>
                </v-col>
                <v-col cols="2" class="marginLeft">
                    <v-btn
                      color="green"
                      rounded
                      dark
                      x-large
                      class="py-7 d-none d-sm-none d-md-flex"
                    >
                      search
                    </v-btn>
                  </v-col>
              </v-row>
            </v-card-text>
            </v-img>
          </v-card>
          <v-toolbar flat color="transparent">
            <v-toolbar-title class="text-h5">Category</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn-toggle v-model="toggle_exclusive" group color="#49D9A0">
              <v-btn>
                <v-icon>mdi:mdi-chevron-left</v-icon>
              </v-btn>
              <v-btn>
                <v-icon>mdi:mdi-chevron-right</v-icon>
              </v-btn>
            </v-btn-toggle>
          </v-toolbar>
          <!-- category -->
          <category/>

          <v-toolbar flat color="transparent" class="mt-5">
            <v-toolbar-title class="text-h5">Popular Product</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn rounded color="green" dark class="px-8">See All</v-btn>
          </v-toolbar>
            <!-- product -->
          <Product />
          <v-card flat color="#E2F2E5" class="rounded-xl mt-8">
            <v-toolbar flat color="transparent" class="mb-4">
              <v-toolbar-title class="text-h6 mt-5"
                >Popular Bundle Pack</v-toolbar-title
              >
              <v-spacer></v-spacer>
            </v-toolbar>

            <!-- pack -->
            <Pack />
          </v-card>
          <v-card flat color="#FAFAFA" class="mt-8 py-5 px-16">
            <div
              style="
                position: absolute;
                margin-left: auto;
                margin-right: auto;
                left: 0;
                right: 0;
                text-align: center;
              "
            >
              <h3>What Our Clients Say</h3>
            </div>

            <!-- client -->
            <Client />
          </v-card>
          <v-toolbar flat color="transparent" class="mt-8" style="text-align: center;">
            <v-toolbar-title class="text-h5" 
              >Our Trusted Partner</v-toolbar-title
            >
          </v-toolbar>

          <!-- partner -->
          <Partner />
          
          <v-card
            flat
            color="#E2F2E5"
            class="rounded-xl mtop mbottom mx-10 pa-4"
            height="350"
          >
            <v-row>
              <v-col cols="12" xs="12" sm="12" md="5">
                <v-card
                  
                  height="450px"
                  width="200px"
                >
                  <v-img src="../public/mobile.png"></v-img>
                </v-card>
              </v-col>
              <v-col cols="12" xs="12" sm="6" md="7">
                <h1 class="mt-16">Download App</h1>
                <p>
                  Lorem ipsum dolor sit amet consectetur adipisicing elit.<br />
                  Provident sequi esse tempore maiores quasi quia non.<br />
                  Itaque laboriosam dicta nostrum accusantium assumenda,<br />
                  vitae ab ut vel tenetur minima natus commodi!
                </p>
                <v-btn color="black" dark class="mb-10">
                  <v-icon color="white" left>fab fa-apple</v-icon>
                  App Store
                </v-btn>
                <v-btn color="black" dark class="ml-4 mb-10">
                  <v-icon color="white" left>fab fa-google-play</v-icon>
                  Play Store
                </v-btn>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
    <!-- footer -->
    <Footer/>
    
  </v-app>
</template>

<script>
import { defineComponent } from 'vue';

// Components
import Navbar from '../components/Navbar.vue';
import Category from '../components/Category.vue';
import Product from '../components/Product.vue';
import Pack from '../components/Pack.vue';
import Client from '../components/Client.vue';
import Partner from '../components/Partner.vue';
import Footer from "../components/Footer.vue";

export default defineComponent({
  name: 'HomeView',
  data: () => ({
    toggle_exclusive: 1,
  }),

  components: {
    Navbar,
    Category,
    Product,
    Pack,
    Client,
    Partner,
    Footer

  },
});
</script>
<style >
.marginLeft {
  margin-left: -90px;
}
.mtop {
  margin-top: 100px;
  
}
.mbottom {
  margin-bottom: 100px;
}
.v-card.borderme {
  border: 2px solid green !important;
}
.v-card.borderout {
  border: 1px solid #d5f0db !important;
}
.v-btn:not(.v-btn--round).v-size--default.add {
  min-width: 0px !important;
}
.theme--light.v-sheet--outlined.mobile {
  border: 2px solid black !important;
}
@media only screen and (max-width: 600px) {
  h2.title1 {
    font-size: 15px;
  }
  h2.title2 {
    font-size: 15px;
  }
  .top {
    margin-top: 20px;
  }
}
@media only screen and (min-width: 600px) {
  .top {
    margin-top: 70px;
  }
}
@media only screen and (min-width: 768px) {
  .top {
    margin-top: 120px;
  }
}
</style>
