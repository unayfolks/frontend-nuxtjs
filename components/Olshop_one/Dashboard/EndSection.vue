<template>
  <!-- <v-img :src="endpic"  width="100%" cover>
  </v-img> -->
  <v-layout class="d-flex align-center flex-col">
    <v-container class="pb-0">

    <div class="background-image-layout">
      <div class="w-full">
        <v-container
          class="text-center"
          style="background: rgba(84, 146, 146, 0.9)"
        >
          <v-row class="d-flex align-center justify-center">
            <v-col class="text-white" cols="12" lg="3" sm="6">
              <div class="text-center text-h3">Navigation</div>
              <div>
                <ul
                  class="d-lg-block justify-center gap-4 d-sm-block d-xs-flex"
                >
                  <li>Home</li>
                  <li>Shop</li>
                  <li>About</li>
                  <li>Vlog</li>
                  <li>Contact</li>
                  <li>Shipping</li>
                  <li>Privacy Policy</li>
                  <li>Press</li>
                </ul>
              </div>
            </v-col>
            <v-col class="d-flex flex-col text-white">
              <div class="text-h5 text-md-h6" cols="12" lg="3" sm="6">
                Join Our Email list and use 10% off promo code
              </div>
              <v-text-field placeholder="your email address"> </v-text-field>
              <div>
                <v-btn rounded="0" color="cyan" variant="tonal">Join Now</v-btn>
              </div>
            </v-col>
            <v-col class="text-white" cols="12" lg="3" sm="12">
              <div>find Us, Were on Social Media</div>
              <div>
                <ul class="d-flex justify-center gap-2">
                  <li><v-btn icon="mdi-facebook"></v-btn></li>
                  <li><v-btn icon="mdi-instagram"></v-btn></li>
                  <li><v-btn icon="mdi-youtube"></v-btn></li>
                </ul>
              </div>
            </v-col>
          </v-row>
        </v-container>
      </div>
      <div class="w-full">
        <v-container
          style="background: rgba(84, 146, 146, 0.9)"
          class="border-t-2"
        >
          <v-row>
            <v-col>&copy; 2024. All right Reserved. Stretch It Out</v-col>
            <v-col class="text-right">
              <div>
                made with <span> <v-icon>mdi-heart</v-icon> </span> by ellcodes
              </div>
            </v-col>
          </v-row>
        </v-container>
      </div>
    </div>
  </v-container>

  </v-layout>
</template>

<script lang="ts" setup></script>

<style>
.background-image-layout {
  background-image: url("@/public/img/olshopone/dashboard/endimg.webp");
  background-size: cover;
  background-position: center;
}
</style>
