<template>
    <div class="py-10">
        <v-parallax :src="grid5" height="500px">
            <v-container class="py-10 fill-height">
                <v-row >
                    <v-spacer></v-spacer>
                    <v-col class="col-12 col-md-8 col-lg-6    ">
                        <h1 class="text-left text-h4 text-white">COOPERATION OBJECTIVES</h1>
                        <p class="text-left text-white">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, quos.
                        </p>
                        <v-btn class="mt-5">
                            Read More
                        </v-btn>
                    </v-col>
                </v-row>
            </v-container>
        </v-parallax>
        
        <!-- <img :src="grid5" alt="grid5" class="position-sticky"> -->
    </div>
</template>
<script setup>
import grid5 from '@/public/img/espor/pic_5.webp'


</script>

