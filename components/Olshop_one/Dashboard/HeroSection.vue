<template>
  <div class="mt-50">
    <v-container>
      <v-img :src="background" cover :height="'75vh'" style="">
        <v-row class="fill-height">
          <v-col class=" d-lg-block d-sm-none d-md-none"  cols="12" md="6" sm="12">

          </v-col>
          <v-col class=" d-flex justify-center align-lg-start align-sm-center align-md-center flex-col ga-5" cols="12" md="6" sm="12">
            <div class="border-x-4 border-y-4 text-h3 pa-4 text-cyan-500">
              Get Now
            </div>
            <div class="text-h4 text-white">
              Best Mens Clothes
            </div>
            <v-btn rounded="0" color="cyan" variant="outlined">
              Learn More
            </v-btn>
          </v-col>
        </v-row>
      </v-img>
    </v-container>
    <!-- <div class="text-h5">Hero</div> -->
  </div>
</template>

<script lang="ts" setup>
import background from '@/public/img/olshopone/dashboard/heroimg.webp'
</script>

<style>

</style>