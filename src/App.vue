<template>
  <v-app>  
    <v-app-bar app color="primary" dark>  
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title to="/">{{ appName }}</v-toolbar-title>          
    </v-app-bar>
        
    <v-content>
      <v-container fluid>
        <FormKtp />
      </v-container>
    </v-content>

    <v-card>
      <v-footer absolute app>
        <v-card-text class="text-center">
          &copy; {{ new Date().getFullYear() }} — <strong>KIOSK</strong>
        </v-card-text>
      </v-footer>
    </v-card>
  
  </v-app>
</template>

<script>

export default {
  name: 'App',
  components: {
  //  Header: () => import( /* webpackChunckName: "header" */ '@/components/layouts/Header.vue'),
   // HelloWorld: () => import( /* webpackChunckName: "helloworld" */ '@/components/HelloWorld.vue'),    
    FormKtp: () => import( /* webpackChunckName: "formktp" */ '@/components/form-ktp/FormKtp.vue')    
    // Alert: () => import( /* webpackChunkName: "alert" */ '@/components/Alert.vue'),
    // Search: () => import( /* webpackChunkName: "search" */ '@/components/Search.vue'),
    // Login: () => import( /* webpackChunkName: "login" */ '@/components/Login.vue'),
    // Register: () => import( /* webpackChunkName: "register" */ '@/components/Register.vue'),
    // Cart: () => import( /* webpackChunkName: "cart" */ '@/components/Cart.vue'),    
  },
    
};
</script>
