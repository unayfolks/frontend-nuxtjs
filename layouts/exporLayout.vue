<template>
  <v-app>
    <exporDashboardNavbarSection />
    <slot />
    <exporDashboardFooterSection />
    <v-fab
      icon="mdi-whatsapp"
      class="ma-4 mr-10"
      color="green"
      location="bottom end"
      size="64"
      sticky
      app
      appear
    ></v-fab>
  </v-app>
</template>
