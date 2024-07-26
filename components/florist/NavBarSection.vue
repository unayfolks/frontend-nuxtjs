<template>
    <v-sheet class="background-image-layout">
        <v-row>
            <v-col cols="12" class="text-center mt-2">
                <div>
                    <div class="text-h3 text-center text-red-600">
                        IfahAgnes
                    </div>
                    <div class=" text-h4 text-center">
                        florist
                    </div>
                </div>
            </v-col>
            <v-col colss="12">
                <ul class="-mt-5 d-flex gap-5 justify-center text-center ">
                    <li>
                        <NuxtLink to="/florist">Home</NuxtLink>
                    </li>
                    <li>
                        <NuxtLink to="/florist/catalogue">Catalogue</NuxtLink>
                    </li>
                    <li><NuxtLink to="/florist/service">Our Service</NuxtLink></li>
                    <li><NuxtLink to="/florist/about">About Us</NuxtLink></li>
                    <li><NuxtLink to="/florist/contact">Contact</NuxtLink></li>
                    
                </ul>
            </v-col>
        </v-row>
    </v-sheet>
    <v-app-bar scroll-behavior="hide inverted" class="" height="80"
        style="border-bottom: 2px solid black; " inverted>
        <v-app-bar-title class="">
            <v-container>
                <v-row class="">
                    <v-col class=" d-flex justify-start" >
                        <!-- <Icon name="uil:flower" color="black" size="3em" /> -->
                        <div>
                            <div class="text-h5 text-center text-red-600">
                                IfahAgnes
                            </div>
                            <div class="text-subtitle-2 text-center">
                                florist
                            </div>
                        </div>
                    </v-col>
                    
                    <v-col class=" d-none d-sm-none d-md-flex align-center justify-end">
                        <div>
                            <v-btn icon="mdi-cart"></v-btn>
                        </div>
                    </v-col>
                    <v-col class="d-md-none d-sm-flex d-flex align-center  justify-end ">
                        <div>
                            <v-btn icon="mdi-menu"  @click.stop="drawer = !drawer"></v-btn>
                        </div>
                    </v-col>
                </v-row>
            </v-container>

        </v-app-bar-title>

    </v-app-bar>
    <v-navigation-drawer v-model="drawer" temporary rail rail-width="1000" class="bg-slate-200">
        <v-col>

            <v-list density="compact" nav>
                <v-list-item title="Home" value="home"></v-list-item>
                <v-divider></v-divider>
                <v-list-item title="Catalogue" value="catalogue"></v-list-item>
                <v-divider></v-divider>
                <v-list-item title="Our Service" value="our service"></v-list-item>
                <v-divider></v-divider>
                <v-list-item title="Contact" value="contacts"></v-list-item>
                <v-divider></v-divider>
            </v-list>
        </v-col>
        <v-spacer/>
        <v-col class=" d-flex fill-height justify-center align-center">
            <v-sheet class="text-center">
                <div>
                    <div class="text-h5 text-center text-red-600">
                        IfahAgnes
                    </div>
                    <div class="text-subtitle-2 text-center">
                        florist
                    </div>
                </div>
                <div>
                    <div class="text-h5 text-center">
                        083119050309
                    </div>
                    <div class="text-subtitle-2 text-center">
                        address: Jl. alamat dst
                    </div>
                </div>
            </v-sheet>
        </v-col>
    </v-navigation-drawer>
</template>
<script>
export default {
    data() {
        return {
            drawer: false
        }
    },
}

</script>
<style scoped>
.background-image-layout {
    background-image: url("@/public/img/florist/bestone.webp");
    background-size: cover;
    background-position: center;
  }
</style>