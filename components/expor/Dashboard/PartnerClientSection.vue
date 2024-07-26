<template>
  <div class="mt-10 bg-slate-200">
    <v-container>
      <div class="py-10">
        <v-row class="d-flex align-center ">
          <v-col cols="12" md="6">
            <UCarousel
              ref="carouselRef"
              v-slot="{ item }"
              :items="items"
              :ui="{ item: 'basis-full md:basis-1/2 lg:basis-1/2' }"
              class="rounded-lg overflow-hidden"
            >
              <img :src="item" class="w-full" draggable="false" />
            </UCarousel>
          </v-col>
          <v-col cols="12" md="6">
            <div>
              <v-card-text class="text-h3"
                >Our Partner and Client</v-card-text
              >
              <v-carousel
                cycle
                hide-delimiters
                :show-arrows="false"
                :continuous="true"
                height="auto"
              >
                <v-carousel-item v-for="(name, i) in names" :key="i">
                  <div class="  ">
                    <v-sheet color="transparent">
                      <v-card-title class="text-h5">{{ name }}</v-card-title>
                      <v-card-text>{{ comments[i] }}</v-card-text>
                      <v-card-text>{{ profesi[i] }}</v-card-text>
                    </v-sheet>
                  </div>
                </v-carousel-item>
              </v-carousel>
            </div>
          </v-col>
        </v-row>
      </div>
    </v-container>
  </div>
</template>

<script lang="ts" setup>
import grid1 from "@/public/img/espor/logo/logo_1.webp";
import grid2 from "@/public/img/espor/logo/logo_2.webp";
import grid3 from "@/public/img/espor/logo/logo_3.webp";
import grid4 from "@/public/img/espor/logo/logo_4.webp";
import grid5 from "@/public/img/espor/logo/logo_5.webp";

const items = [grid1, grid2, grid3, grid4, grid5];
const names = ["name 1", "name 2", "name 3", "name 4", "name 5", "name 6"];
const comments = [
  "lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.",
  "lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.",
  "lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.",
  "lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.",
  "lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.",
  "lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.",
];
const profesi = [
  "Designer",
  "Developer",
  "Designer",
  "Developer",
  "Designer",
  "Developer",
];
const carouselRef = ref();

onMounted(() => {
  setInterval(() => {
    if (!carouselRef.value) return;

    if (carouselRef.value.page === carouselRef.value.pages) {
      return carouselRef.value.select(0);
    }

    carouselRef.value.next();
  }, 3000);
});
</script>

<style></style>
