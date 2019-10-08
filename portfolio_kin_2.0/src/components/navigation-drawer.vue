<template>
  <div>
    <v-navigation-drawer
      v-model="drawer"
      app
      expand-on-hover
      color="blue-grey darken-2 white--text"
    >
      <v-list dense nav>
        <v-list-item>
          <v-avatar tile>
            <img src="../assets/crow.png" alt="Crow" />
          </v-avatar>
          <v-list-item-content>
            <v-list-item-title class="title">Curriculum Vitae</v-list-item-title>
            <v-list-item-subtitle>Cheung Kin Wong</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>

        <v-divider></v-divider>
        <v-list-item v-for="item in items" :key="item.title" link :href="item.url">
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar app collapse-on-scroll color="blue-grey darken-2">
      <div class="flex-grow-1"></div>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
    </v-app-bar>
    <v-footer app>
      <span>&copy; 2019</span>
    </v-footer>
  </div>
</template>

<script>
export default {
  name: "NavigationDrawer",
  data: () => ({
    items: [
      { title: "Home", icon: "mdi-home", url: "#home" },
      { title: "Info", icon: "mdi-xml", url: "#info" },
      { title: "Projects", icon: "mdi-folder-multiple", url: "#projects" },
      { title: "About me", icon: "mdi-information", url: "#aboutme" }
    ],
    drawer: null
  }),
  created() {
    this.$vuetify.theme.dark = true;
  }
};
</script>