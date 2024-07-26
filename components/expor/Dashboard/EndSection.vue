<template>
  <div class="">
    <v-img
      :src="img5"
      class="d-flex align-center justify-center"
      cover
      height="50vh"
      style="filter: grayscale(75%)"
    >
      <v-container>
        <v-row>
          <v-col cols="12" md="6" class="text-white">
            <div>Contact Us</div>
            <div class="d-flex">
              <v-icon>mdi-map</v-icon>
              <div>
                Jl. Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Debitis maiores laboriosam nam! Accusamus laborum enim ex rem
                necessitatibus dolorum, velit recusandae vero in deserunt, iusto
                aliquid deleniti ipsum ratione vitae.
              </div>
            </div>
          </v-col>
          <v-col cols="12" md="6" class="d-flex  justify-center" >
            <iframe
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d987.8688767852038!2d112.65439094578896!3d-7.949713455078317!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2dd629baa16f09ab%3A0xfae32fda46c7dbfd!2sJl.%20Terusan%20Batubara%20V%2047%2C%20Pandanwangi%2C%20Kec.%20Blimbing%2C%20Kota%20Malang%2C%20Jawa%20Timur%2065126%2C%20Indonesia!5e0!3m2!1sen!2sus!4v1721149285544!5m2!1sen!2sus"
              style="border: 0"
              allowfullscreen="false"
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
            ></iframe>
          </v-col>
        </v-row>
      </v-container>
    </v-img>
  </div>
</template>

<script lang="ts" setup>
import img5 from "@/public/img/espor/pic_5.webp";
</script>

<style></style>
