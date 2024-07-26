<template>
  <v-app>
    <floristNavBarSection />
    <slot />
    <v-fab
      icon="mdi-whatsapp"
      class="ms-4 mb-4"
      color="green"
      location="bottom end"
      size="64"
      sticky
      app
      appear
      @click="wame"
    ></v-fab>
    <floristFooterSection />
  </v-app>
</template>
<script>
export default{
  data() {
    return {
      
    }
  },
  methods: {
    wame(){
      window.open('https://wa.me/6283119050309', '_blank');
    }
  },
}

</script>