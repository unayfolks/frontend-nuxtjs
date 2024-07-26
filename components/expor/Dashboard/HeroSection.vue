<template>
    <v-carousel height="75vh" show-arrows="hover" cycle hide-delimiter-background class="mt-8">
        <v-carousel-item v-for="(slide, i) in slides" :key="i">
            <v-sheet color="black" height="100%">
                <v-img :src="car[i]" height="100%" cover style="filter: grayscale(0%);">
                    <div class="d-flex fill-height justify-center align-center" style="background: rgba(0, 0, 0, 0.7)">
                        <v-container >
                            <v-col>
                                <div class="text-h2 text-red" style="border-bottom: 2px solid black;">{{ slide }}</div>
                                <div class="text-lg-h5">{{ desc[i] }}</div>
                                <v-btn color="red" >Read More</v-btn>
                            </v-col>
                        </v-container>
                    </div>
                </v-img>
            </v-sheet>
        </v-carousel-item>
    </v-carousel>
</template>
<script>
import grid1 from '@/public/img/espor/pic_1.webp'
import grid2 from '@/public/img/espor/pic_2.webp'
import grid3 from '@/public/img/espor/pic_3.webp'
export default {
    data() {
        return {
            grid2: grid2,
            grid3: grid3,
            grid1: grid1,

            car: [grid1, grid2, grid3],
            colors: ['indigo', 'warning', 'pink darken-2', 'red lighten-1', 'deep-purple accent-4'],
            slides: [
                'PT. Mapan Expor Indonesia',
                'Our Bussines',
                'Example',
            ],
            desc: [
                'PT. Mapan Expor Indonesia is a business Consulting Company Indonesia. PT. Mapan Expor Indonesia is focus to serve and provide solution to our business partner both local and foreign Company. As Business Consultant, PT. Mapan Expor Indonesia has expertise to support in Biomass, Investment, Development and Contractor, Machinery, Marketing Consultant.',
                'We have businesses in the fields of Agriculture, General Trading, Export and Import and Business Consultants',
                'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dignissimos reprehenderit exercitationem beatae accusantium dolorum aperiam ullam voluptas, delectus obcaecati vitae eum asperiores, amet consectetur architecto fuga deserunt expedita qui deleniti?'
            ]
        }
    },
}
</script>
<style>
.col{
    color: rgb(0, 0, 0);
}
</style>