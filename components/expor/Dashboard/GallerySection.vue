<template>
  <div>
    <v-container>

      <h1 class="text-center text-h3 mb-5" style="border-bottom: 1px solid black;">Gallery</h1>
    </v-container>

    <div class="mx-4">
      <v-row>
        <v-col cols="12" md="4" lg="3" sm="3" v-for="(item, i) in items" :key="item" >
          <img :src="item" alt="grid1"   @click="selectImage(item)"/>
        </v-col>
      </v-row>
    </div>

    <UModal v-model="isOpen">
      <div class="">
        <img :src="selectedImage"  />
        
      </div>
    </UModal>
  </div>
</template>
<script setup lang="ts">
let isOpen = ref(false);
const selectedImage = ref('');
import grid1 from '@/public/img/espor/pic_1.webp'
import grid2 from '@/public/img/espor/pic_2.webp'
import grid3 from '@/public/img/espor/pic_3.webp'
import grid4 from '@/public/img/espor/pic_4.webp'
import grid5 from '@/public/img/espor/pic_5.webp'

const items = [
    grid1,
    grid2,
    grid3,
    grid4,
    grid5
]

const selectImage = (image: string) => {
    isOpen.value = true;
    selectedImage.value = image;
}
</script>
<style scoped></style>