<template>
    <div class="py-10">
        <v-container>
            <h1 class="text-center text-h3" style="border-bottom: 1px solid black;">Comodities</h1>
        </v-container>
        <UContainer>

            <UCarousel v-slot="{ item }" :items="items" :ui="{ item: 'basis-full md:basis-1/2 lg:basis-1/3' }"
                indicators class="rounded-lg overflow-hidden">
                <v-card class="ma-2">
                    <img :src="item" class="w-full" draggable="false">
                    <v-card-title>{{ titles[items.indexOf(item)] }}</v-card-title>
                    <v-card-text>{{ descriptions[items.indexOf(item)] }}</v-card-text>
                </v-card>
            </UCarousel>
        </UContainer>
    </div>
</template>
<script setup lang="ts">
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
const titles = [
    'Tomato',
    'Grape',
    'Radish',
    'Carrot',
    'Coffee'
]
const descriptions = [
    'Tomato is a fruit that is used in many dishes.',
    'Grape is a fruit that is used in many dishes.',
    'Radish is a vegetable that is used in many dishes.',
    'Carrot is a vegetable that is used in many dishes.',
    'Coffee is a drink that is used in many dishes.'
]

</script>
