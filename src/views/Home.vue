<template>
  <div class="home" style="background-color: #ffec0c;">
    <v-container>
      <v-card
        elevation="10"
        outlined
        id="bannercard"
        style="background-color: #ffec0c; border: none;"
      >
        <v-container>
          <v-row class="mb-6" no-gutters>
            <v-col sm="5" md="5">
              <img
                alt="Usine Nantek logo"
                src="../assets/usinenanteklogo1.png"
                id="logo"
              />
            </v-col>
            <v-col sm="7" md="7">
              <p id="bannertext" style="">
                <strong>Vivez une nouvelle expérience !</strong>
              </p>
            </v-col>
          </v-row>
        </v-container>
        <v-btn  elevation="2"  x-large id="btnstart"
          ><v-icon style="color: white"> mdi-rocket </v-icon> &nbsp; <span id="textbtnstart"><strong>Lancer</strong></span>
        </v-btn>
      </v-card>
    </v-container>
    <v-footer padless style="margin-top: 50px; background-color: #ffec0c">
      <v-card
        flat
        tile
        class="text-center col-12"
        style="background-color: #ffec0c"
      >
        <v-card-text>
          <v-btn
            v-for="icon in icons"
            :key="icon"
            class="mx-4 white--text"
            icon
          >
            <v-icon size="24px">
              {{ icon }}
            </v-icon>
          </v-btn>
        </v-card-text>
        <v-card-text class="white--text">
          {{ new Date().getFullYear() }} | <strong>l'Usine Nantek</strong>
        </v-card-text>
      </v-card>
    </v-footer>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  data() {
    return {
      dialog: false,
      icons: ["mdi-email", "mdi-instagram"],
    };w 
  },
  name: "Home",
  components: {
    HelloWorld,
  },
};
</script>

<style>
#bannercard {
  margin-top: 100px;
  width: 100%;
  height: 500px;
}

#btnstart {
  margin: 15px;
  background-color: #3555a2;
  margin-left: 300px;
}

#btnstart:hover {
  background-color: #2177c7;
}

#textbtnstart{
  color: white;
  font-size: 22px;
  margin-left: 10px;
}
#logo {
  width: 250px;
  height: 250px;
  float: right;
  margin-right: 100px;
}
#bannertext {
  font-size: 48px;
  margin-top: 100px;
  color: #3555a2;
  float: left;
}
</style>
