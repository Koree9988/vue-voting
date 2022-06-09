<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer" app>
      <!--  -->
      <v-list dense nav>
        <v-list-item link to="/">
          <v-list-item-icon>
            <v-icon>mdi-home</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item link to="/vote">
          <v-list-item-icon>
            <v-icon>mdi-allergy</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>Vote</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
         <v-list-item link to="/covid/data">
          <v-list-item-icon>
            <v-icon>mdi-virus</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>Civid Data</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

    </v-navigation-drawer>

    <v-app-bar app>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Application</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <!--  -->
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    drawer: null,
  }),
};
</script>
