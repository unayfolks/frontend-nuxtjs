<template>
  <v-layout>
    <v-container>
      <v-row>
        <v-col cols="12" md="3">
          <v-list>
            <v-list-item title="" cursor="pointer"
              ><NuxtLink to="#">New Arrival</NuxtLink></v-list-item
            >
            <v-list-item title="" cursor="pointer"
              ><NuxtLink to="#">On Sale</NuxtLink></v-list-item
            >
            <v-list-group value="Mens">
              <template v-slot:activator="{ props }">
                <v-list-item v-bind="props" title="Mens"></v-list-item>
              </template>
              <v-list-item v-for="(men, i) in mens" :key="i" :value="men.id">{{
                men.name
              }}</v-list-item>
            </v-list-group>
            <v-list-group value="Womens">
              <template v-slot:activator="{ props }">
                <v-list-item v-bind="props" title="Womens"></v-list-item>
              </template>
              <v-list-item
                v-for="([women], i) in womens"
                :key="i"
                :title="women"
                :value="women"
              ></v-list-item>
            </v-list-group>
            <v-list-group value="Accessories">
              <template v-slot:activator="{ props }">
                <v-list-item v-bind="props" title="Accessories"></v-list-item>
              </template>
              <v-list-item
                v-for="([acc], i) in accessories"
                :key="i"
                :title="acc"
                :value="acc"
              ></v-list-item>
            </v-list-group>
          </v-list>
        </v-col>
        <v-col cols="12" md="9">
          <v-row>
            <v-col
              cols="12"
              md="6"
              lg="4"
              sm="6"
              xs="6"
              v-for="(produk, i) in products"
              :key="i"
            >
              <v-hover >
                <template v-slot:default="{ props: hoverProps, isHovering }">
                  <v-card
                  @click="seemore(produk)"
                    rounded="0"
                    elevation="0"
                    class="border-thin"
                    v-bind="hoverProps"
                    :class="[
                      'mx-auto',
                      isHovering ? 'opacity-50' : 'opacity-100',
                    ]"
                  >
                    <v-img :src="produk.img">
                      <v-overlay
                        :model-value="isHovering"
                        class="align-center justify-center"
                        scrim="#549292"
                        contained
                      >
                        <v-btn
                          variant="flat"
                          elevation="0"
                          rounded="0"
                          color="cyan"
                         
                          >See more info</v-btn
                        >
                      </v-overlay>
                    </v-img>
                    <v-card-title>
                      {{ produk.title }}
                    </v-card-title>
                    <v-card-item class="text-right pa-5">
                      <v-btn rounded="0" color="black">
                        {{ produk.price }}
                      </v-btn>
                    </v-card-item>
                  </v-card>
                </template>
              </v-hover>
            </v-col>
          </v-row>
          <!-- <v-pagination :length="20"></v-pagination> -->
        </v-col>
      </v-row>
    </v-container>
  </v-layout>
  <v-dialog v-model="dialogdetail" width="auto">
    <v-card rounded="0" elevation="0" max-width="75vh">
      <div class="d-sm-block d-md-flex">
        <div class="d-flex align-start justify-start">
          <v-img
            :src="imgdetail"
            cover
            height="auto"
            width="400"
            class="ma-4"
          ></v-img>
        </div>
        <div class="ma-4 ">
          <div>
            <v-card-title class="text-h4">{{ titledetail }}</v-card-title>
            <v-card-subtitle>{{ pricedetail }}</v-card-subtitle>
          </div>
          <div>
            <v-row>
              <v-col >
                <v-card-subtitle>Size</v-card-subtitle>
                <v-item-group mandatory>
                  <v-container>
                    <v-row>
                      <v-col v-for="n in size" :key="n" cols="12" md="3" lg="3" sm="3" xs="3">
                        <v-item v-slot="{ isSelected, toggle }">
                          <v-card
                            :color="isSelected ? 'primary' : ''"
                            class="d-flex align-center justify-center"
                            height="40"
                            width="40"
                            rounded="circle"
                            dark
                            @click="toggle"
                          >
                            <v-scroll-y-transition>
                              <div class="text-h6 text-center">
                                {{ isSelected ? n : n }}
                              </div>
                            </v-scroll-y-transition>
                          </v-card>
                        </v-item>
                      </v-col>
                    </v-row>
                  </v-container>
                </v-item-group>
              </v-col>
            </v-row>
            <v-row>
              <v-col>
                <v-card-subtitle>Color</v-card-subtitle>
                <v-item-group mandatory>
                  <v-container>
                    <v-row>
                      <v-col v-for="n in color" :key="n"  cols="12" md="3" lg="3" sm="3" xs="3" >
                        <v-item v-slot="{ isSelected, toggle }">
                          <v-card
                            :color="isSelected ? n : n"
                            class="d-flex align-center justify-center"
                            height="40"
                            width="40"
                            rounded="circle"
                            dark
                            @click="toggle"
                          >
                            <v-scroll-y-transition>
                              <div class="text-h6 text-center">
                                <v-icon>
                                  {{ isSelected ? "mdi-check" : "" }}
                                </v-icon>
                              </div>
                            </v-scroll-y-transition>
                          </v-card>
                        </v-item>
                      </v-col>
                    </v-row>
                  </v-container>
                </v-item-group>
              </v-col>
            </v-row>
            <v-row>
              <v-col > 
                <v-number-input
                  label="Quantity"
                  control-variant="split"
                  :min="1"
                  :model-value="1"
                  :hideInput="false"
                  :inset="false"
                  variant="outlined"
                ></v-number-input>
              </v-col>
            </v-row>
            <v-row >
              <v-card-text :max-width="200">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores doloribus dolores cum nemo velit? Veniam recusandae quas perspiciatis eaque maxime asperiores voluptas cum, amet rem cupiditate dolorum unde. Magni, fugit?
              </v-card-text>
            </v-row>
            <v-row>
              <v-col>
                <v-btn rounded="0" color="cyan" @click="dialogdetail = false"
                  >Add to Cart</v-btn
                >
              </v-col>
            </v-row>
          </div>
        </div>
      </div>
    </v-card>
  </v-dialog>
</template>
<script>
import prod10 from "@/public/img/olshopone/dashboard/10.webp";
import prod11 from "@/public/img/olshopone/dashboard/11.webp";
import prod12 from "@/public/img/olshopone/dashboard/12.webp";
import prod13 from "@/public/img/olshopone/dashboard/13.webp";
import prod14 from "@/public/img/olshopone/dashboard/14.webp";
import prod15 from "@/public/img/olshopone/dashboard/15.webp";
import prod16 from "@/public/img/olshopone/dashboard/16.webp";
import prod17 from "@/public/img/olshopone/dashboard/17.webp";
import prod18 from "@/public/img/olshopone/dashboard/18.webp";
import prod19 from "@/public/img/olshopone/dashboard/19.webp";
import prod20 from "@/public/img/olshopone/dashboard/20.webp";
import prod21 from "@/public/img/olshopone/dashboard/21.webp";
import { VNumberInput } from "vuetify/labs/VNumberInput";

export default {
  components: {
    VNumberInput,
  },
  data: () => ({
    size: ["S", "M", "L", "XL"],
    color: ["red", "blue", "green", "black"],
    dialogdetail: false,
    products: [
      {
        img: prod10,
        title: "tshirt stretch out",
        price: "Rp. 25.000",
      },
      {
        img: prod11,
        title: "tshirt coffee",
        price: "Rp. 25.000",
      },
      {
        img: prod12,
        title: "Jeans jacket",
        price: "Rp. 25.000",
      },
      {
        img: prod13,
        title: "tshirt stretch it out black",
        price: "Rp. 25.000",
      },
      {
        img: prod14,
        title: "Coboy hat",
        price: "Rp. 50.000",
      },
      {
        img: prod15,
        title: "Tompi hat",
        price: "Rp. 50.000",
      },
      {
        img: prod16,
        title: "Boot green",
        price: "Rp. 150.000",
      },
      {
        img: prod17,
        title: "Sneakers black white",
        price: "Rp. 150.000",
      },
      {
        img: prod18,
        title: "Running Shoes",
        price: "Rp. 150.000",
      },
      {
        img: prod19,
        title: "Sport Shoes",
        price: "Rp. 150.000",
      },
      {
        img: prod20,
        title: "Sneakers sport school",
        price: "Rp. 150.000",
      },
      {
        img: prod21,
        title: "Sneakers school",
        price: "Rp. 150.000",
      },
    ],
    mens: [
      {
        id: "01",
        name: "T-Shirt",
      },
      {
        id: "02",
        name: "Tank Top",
      },
      {
        id: "03",
        name: "Long Pants",
      },
      {
        id: "04",
        name: "Short Pants",
      },
      {
        id: "05",
        name: "Long Sleve",
      },
    ],
    womens: [
      ["T-Shirt"],
      ["Tank Top"],
      ["Long Pants"],
      ["Short Pants"],
      ["Long Sleve"],
      ["Shoes"],
      ["Sport"],
      ["Shirt"],
      ["Suit"],
    ],
    accessories: [
      ["Hat"],
      ["Beanies"],
      ["Belt"],
      ["Wallets"],
      ["Sock"],
      ["Sunglasses"],
      ["Pins"],
    ],
  }),
  methods: {
    seemore(produk) {
      this.dialogdetail = true;
      this.imgdetail = produk.img;
      this.titledetail = produk.title;
      this.pricedetail = produk.price;
    },
  },
};
</script>
<!-- <script lang="ts" setup>
const kategori = [
  {
    judul: "New Arival",
  },
  {
    judul: "All Items",
  },
  {
    judul: "Onsale",
  },
  {
    judul: "Mens",
  },
  {
    judul: "Womens",
  },
  {
    judul: "Accessories",
  },
];
const open = ["Users"];
const admins = [
  ["Management", "mdi-account-multiple-outline"],
  ["Settings", "mdi-cog-outline"],
];
const cruds = [
  ["Create", "mdi-plus-outline"],
  ["Read", "mdi-file-outline"],
  ["Update", "mdi-update"],
  ["Delete", "mdi-delete"],
];
</script> -->
<style></style>
