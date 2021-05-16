<template>
  <v-container>
    <v-row class="text-center">
      <!-- <v-col cols="12">
        <v-img
          :src="require('../assets/logo.svg')"
          class="my-3"
          contain
          height="200"
        />
      </v-col> -->

      <v-col class="mb-1">
        <h1 class="display-2 font-weight-normal mb-1">
          Welcome to KIOSK
        </h1>

        <p class="subheading font-weight-regular">
          PELAYANAN PEMDES GELANGKULON
          <br>KECAMATAN SAMBUNG
          <br>KABUPATEN PONOROGO
        </p>
      </v-col>

      <v-col class="mb-5" cols="12">
        <v-row>
          <v-card class="col-5 mr-1">
            <v-card-content>
              <a href=""><h1>BUKU TAMU</h1></a>
            </v-card-content>            
          </v-card>
          <v-col class="2"></v-col>
          <v-card class="col-5 ml-4">
            <v-card-content>
              <a href=""><h1>PELAYANAN</h1></a>
            </v-card-content>            
          </v-card>
        </v-row>        
      </v-col>
      
    </v-row>
  </v-container>
</template>

<script>
  export default {
    name: 'HelloWorld',

    data: () => ({
      ecosystem: [
        {
          text: 'vuetify-loader',
          href: 'https://github.com/vuetifyjs/vuetify-loader',
        },
        {
          text: 'github',
          href: 'https://github.com/vuetifyjs/vuetify',
        },
        {
          text: 'awesome-vuetify',
          href: 'https://github.com/vuetifyjs/awesome-vuetify',
        },
      ],
      importantLinks: [
        {
          text: 'Documentation',
          href: 'https://vuetifyjs.com',
        },
        {
          text: 'Chat',
          href: 'https://community.vuetifyjs.com',
        },
        {
          text: 'Made with Vuetify',
          href: 'https://madewithvuejs.com/vuetify',
        },
        {
          text: 'Twitter',
          href: 'https://twitter.com/vuetifyjs',
        },
        {
          text: 'Articles',
          href: 'https://medium.com/vuetify',
        },
      ],
      whatsNext: [
        {
          text: 'Explore components',
          href: 'https://vuetifyjs.com/components/api-explorer',
        },
        {
          text: 'Select a layout',
          href: 'https://vuetifyjs.com/getting-started/pre-made-layouts',
        },
        {
          text: 'Frequently Asked Questions',
          href: 'https://vuetifyjs.com/getting-started/frequently-asked-questions',
        },
      ],
    }),
  }
</script>
