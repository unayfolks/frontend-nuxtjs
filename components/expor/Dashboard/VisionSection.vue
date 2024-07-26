<template>
  <div class="py-10 bg-slate-200">
    <v-container class="position-relative">
      <v-row>
        <v-col cols="12" md="8" sm="6">
          <h1 class="text-center text-h3 ma-10">Our Vision</h1>
          <v-row>
            <v-col cols="12" md="6">
              <div class="flex">
                <v-btn icon="mdi-plus" size="x-large" color="red"></v-btn>
                <div class="ml-2">
                  <div class="text-h5 text-left">Value +</div>
                  <div class="text-subtitle-2 text-center">
                    Provide added value to stakeholders.
                  </div>
                </div>
              </div>
            </v-col>
            <v-col cols="12" md="6">
              <div class="flex">
                <v-btn icon="mdi-earth" size="x-large" color="red"></v-btn>
                <div class="ml-2">
                  <div class="text-h5 text-left">Global Standart</div>
                  <div class="text-subtitle-2 text-center">
                    Produce global standard products.
                  </div>
                </div>
              </div>
            </v-col>
            <v-col cols="12" md="6">
              <div class="flex">
                <v-btn icon="mdi-human" size="x-large" color="red"></v-btn>
                <div class="ml-2">
                  <div class="text-h5 text-left">Stakeholder</div>
                  <div class="text-subtitle-2 text-left">
                    Company management that takes into account the interests of
                    all stakeholders and environmental interests.
                  </div>
                </div>
              </div>
            </v-col>
            <v-col cols="12" md="6">
              <div class="flex">
                <v-btn icon="mdi-cloud" size="x-large" color="red"></v-btn>
                <div class="ml-2">
                  <div class="text-h5 text-left">Climate Change</div>
                  <div class="text-subtitle-2 text-left">
                    Support climate change programs.
                  </div>
                </div>
              </div>
            </v-col>
          </v-row>
        </v-col>
        <v-col cols="12" md="4" sm="6" class="">
          <v-sheet
            class="position-absolute sm:position-relative right-9 -top-20 sm:w-100"
            color="red"
            elevation="12"
            width="30%"
          >
            <v-card>
              <v-card-title class="text-center">Values</v-card-title>
              <v-devider></v-devider>
              <v-card-text style="border-bottom: 1px solid black"
                >LOYALTY</v-card-text
              >
              <v-card-text style="border-bottom: 1px solid black"
                >HONESTY</v-card-text
              >
              <v-card-text style="border-bottom: 1px solid black"
                >INTEGRITY</v-card-text
              >
              <v-card-text style="border-bottom: 1px solid black"
                >RELIABILITY</v-card-text
              >
              <v-card-text style="border-bottom: 1px solid black"
                >TRANSPARENCY</v-card-text
              >
            </v-card>
          </v-sheet>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<style>
@media (max-width: 600px) {
  .sm\:position-relative {
    position: static !important;
  }
  .sm\:w-100 {
    width: 100% !important;
  }
}
</style>
