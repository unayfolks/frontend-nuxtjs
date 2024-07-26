<template>
  <v-layout>
    <v-app-bar scroll-behavior=" inverted hide" scroll-threshold="200">
      <v-container>
        <v-app-bar-title>
          <v-row class="d-flex align-center">
            <v-col class="d-none d-sm-none d-md-flex">
              <ul class="d-flex ga-5">
                <li>
                  <v-menu open-on-hover transition="slide-x-transition">
                    <template v-slot:activator="{ props }">
                      <div v-bind="props" class="cursor-pointer">Shop</div>
                      <!-- <v-btn color="primary" v-bind="props"> Dropdown </v-btn> -->
                    </template>
                    <v-card
                      class="mx-auto"
                      width="400"
                      color="transparent"
                      variant="plain"
                    >
                      <v-list>
                        <v-list-item
                          v-for="(item, index) in kolor"
                          :key="index"
                          color="transparent"
                        >
                          <v-list-item-title class="cursor-pointer">{{
                            item.title
                          }}</v-list-item-title>
                        </v-list-item>
                      </v-list>
                    </v-card>
                  </v-menu>
                </li>
                <li>About</li>
                <li>Vlog</li>
                <li>Contact</li>
              </ul>
            </v-col>
            <v-col class="d-flex align-start justify-start">
              <v-img :src="logo" height="50" class="my-10"></v-img>
            </v-col>
            <v-col class="d-md-none d-flex align-end justify-end"
              ><v-icon>mdi-menu</v-icon></v-col
            >

            <v-col class="d-none d-sm-none d-md-flex">
              <ul class="d-flex ga-5 float-end float-md-none">
                <li>Login</li>
                <li>Register</li>
                <li><v-icon>mdi-cart</v-icon>Cart</li>
                <li><v-icon>mdi-magnify</v-icon></li>
              </ul>
            </v-col>
          </v-row>
        </v-app-bar-title>
      </v-container>
    </v-app-bar>
    <v-card class="w-full">
      <v-row class="flex-col flex-sm-row">
        <v-col cols="12" lg="12" md="12" sm="6" class="mt-sm-0 mt-lg-10">
          <v-img :src="logo" :height="50" class="py-10"></v-img>
        </v-col>
        <v-col
          cols="12"
          lg="12"
          md="12"
          sm="6"
          class="d-md-none d-flex align-center jcntr pr-10"
          ><v-icon>mdi-menu</v-icon></v-col
        >
        <v-col cols="12" class="d-none d-sm-none d-md-flex">
          <v-container>
            <v-row class="border-t-2">
              <v-col>
                <ul class="d-flex ga-5">
                  <li>
                    <v-menu open-on-hover transition="slide-x-transition">
                      <template v-slot:activator="{ props }">
                        <div v-bind="props" class="cursor-pointer">Shop</div>
                      </template>
                      <v-card
                        class="mx-auto"
                        width="400"
                        color="transparent"
                        variant="plain"
                      >
                        <v-list>
                          <v-list-item
                            v-for="(item, index) in kolor"
                            :key="index"
                            color="transparent"
                          >
                            <v-list-item-title class="cursor-pointer">{{
                              item.title
                            }}</v-list-item-title>
                          </v-list-item>
                        </v-list>
                      </v-card>
                    </v-menu>
                  </li>
                  <li>About</li>
                  <li>Vlog</li>
                  <li>Contact</li>
                </ul>
              </v-col>
              <v-spacer />
              <v-col class="d-none d-sm-none d-md-flex">
                <ul class="d-flex ga-5 float-end float-md-none">
                  <li>Login</li>
                  <li>Register</li>
                  <li><v-icon>mdi-cart</v-icon>Cart</li>
                  <li><v-icon>mdi-magnify</v-icon></li>
                </ul>
              </v-col>
            </v-row>
          </v-container>
        </v-col>
      </v-row>
    </v-card>
  </v-layout>
</template>

<script lang="ts" setup>
import logo from "@/public/img/olshopone/logo.png";
const items = [
  [
    {
      label: "Settings",
      icon: "i-heroicons-cog-8-tooth",
    },
  ],
  [
    {
      label: "Documentation",
      icon: "i-heroicons-book-open",
    },
    {
      label: "Changelog",
      icon: "i-heroicons-megaphone",
    },
    {
      label: "Status",
      icon: "i-heroicons-signal",
    },
  ],
  [
    {
      label: "Sign out",
      icon: "i-heroicons-arrow-left-on-rectangle",
    },
  ],
];
const kolor = [
  { title: "All Product" },
  { title: "New Arrival" },
  { title: "On Sale" },
  { title: "Mens" },
  { title: "Womens" },
  { title: "Accersories" },
];
</script>

<style>
@media (max-width: 960px) {
  .jcntr {
    display: flex;
    justify-content: end;
  }
}
@media (max-width: 600px) {
  .jcntr {
    display: flex;
    justify-content: center;
  }
}

</style>
