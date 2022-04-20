<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">
        
        <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>

        <v-toolbar-title>DISEÑO DE SISTEMAS I</v-toolbar-title>

      </div>


      <v-spacer></v-spacer>

    </v-app-bar>
    
    <v-navigation-drawer v-model="drawer" absolute permanent style="top:65px;height:600px" >
      <v-list nav dense>
        <v-list-item  class="px-16">
            <v-list-item-avatar size="90" center-align>
              <v-img src="https://images.vexels.com/media/users/3/145922/raw/eb6591b54b2b6462b4c22ec1fc4c36ea-creador-de-avatar-femenino.jpg"></v-img>
            </v-list-item-avatar>
          </v-list-item>

          <v-list-item>
            <v-list-item-content>
              <v-list-item-title class="font-size:7px">
                Kenia Stephannie Tepas Mazariego
              </v-list-item-title>
              
              <v-list-item-subtitle>TM17013</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
          <v-divider></v-divider>
          <v-list
          nav
          dense
        >
          <v-list-item link>
            <v-list-item-icon>
              <v-icon>mdi-folder</v-icon>
            </v-list-item-icon>
            <v-list-item-title ><router-link to="/miproyecto">miProyecto</router-link></v-list-item-title>
          </v-list-item>
          <v-list-item link>
            <v-list-item-icon>
              <v-icon>mdi-account-multiple</v-icon>
            </v-list-item-icon>
            <v-list-item-title><router-link to="/miconocimiento">miConocimiento</router-link></v-list-item-title>
          </v-list-item>
          
        </v-list>
        </v-list>

        
    
    </v-navigation-drawer>
    <v-main>
      <router-view />
    </v-main>

    <v-footer dark padless>
      <v-card flat tile class="blue white--text text-center flex " width="100%">
        <v-card-text>
          <v-btn v-for="icon in icons" :key="icon" class="mx-4 white--text" icon>
            <v-icon size="24px">
              {{ icon }}
            </v-icon>
          </v-btn>
        </v-card-text>

        <v-card-text class="white--text pt-0" style="font-size:20px">
          Actividad 2- Intructoria "G2"
        </v-card-text>

      </v-card>
    </v-footer>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
    drawer: false,
    group: null,
    icons: [
      'mdi-facebook',
      'mdi-twitter',
      'mdi-linkedin',
      'mdi-instagram',
    ],
  }),
};
</script>
