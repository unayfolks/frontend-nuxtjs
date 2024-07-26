<template>
    <v-layout style="" class="d-flex flex-col">
        <div class="bg-red-300">
            <v-container class="overflow-auto">
                <ul class="justify-between flex gap-5 text-center ">
                    <li>
                        Simpathy
                    </li>
                    <li>
                        Any Occasion
                    </li>
                    <li>Birthday</li>
                    <li>Love & Birthday</li>
                    <li>Anniversary</li>
                    <li>New Baby</li>
                    <li>Congratulation</li>
                    <li>Thanks</li>
                    <li>Get Well</li>
                </ul>
            </v-container>
        </div>
        <div>
            <v-img :height="'90vh'" aspect-ratio="16/9" cover
                src="/img/florist/floristPict_1.webp">
    
                <div class="d-flex flex-column justify-center align-center fill-height ">
                        <v-sheet style=" " class="ma-4" rounded>
                            <div class="text-h3 ma-2">
                                Your Vision is our Vision
                            </div>
                        </v-sheet>
                        <v-btn>Shop Now</v-btn>
                    
                </div>
    
            </v-img>
        </div>
    </v-layout>
</template>
<!-- <script>
import HeroFoto from '/img/florist/floristPict_1.webp'
export default {
    name: 'HeroSection',
    data() {
        heroFoto : HeroFoto
    }
}
</script> -->