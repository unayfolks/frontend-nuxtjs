<template>
    <!-- <UContainer>
        <UCard class="mt-10">
            <v-icon >mdi-car</v-icon>
            <template #header>
                <div class="flex justify-between">
                    <h1>Welcome to Nuxt UI Starter</h1>
                    <ColorScheme>
                        <USelect v-model="$colorMode.preference" :options="['system', 'light', 'dark']" />
                    </ColorScheme>
                </div>
            </template>
            <UButton icon="i-heroicons-book-open" to="https://ui.nuxt.com" target="_blank">Open Nuxt UI Documentation
            </UButton>
        </UCard>
    </UContainer> -->
    <div>
        <v-container>
            <div class="text-center">
                ellcodes desain template
            </div>
            <div class="text-h4">
                <h1>Index</h1>
            </div>

            <ul>
                <li><NuxtLink to="/florist"> <v-icon>mdi-flower</v-icon>Florist</NuxtLink></li>
                <li><NuxtLink to="/expor"> <v-icon>mdi-earth</v-icon>Expor</NuxtLink></li>
                <li><NuxtLink to="/olshop_one"> <v-icon>mdi-cart</v-icon>Toko Baju</NuxtLink></li>
            </ul>
        </v-container>
    </div>
</template>