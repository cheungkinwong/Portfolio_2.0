<template>
  <v-app>
    <NavigationDrawer></NavigationDrawer>
    <v-content>
      <TheHomePage></TheHomePage>
      <TheInfoPage></TheInfoPage>
      <FirstParallax></FirstParallax>
      <TheProjectsPage></TheProjectsPage>
      <TheAboutPage></TheAboutPage>
    </v-content>
  </v-app>
</template>

<script>
import NavigationDrawer from "./components/navigation-drawer";
import TheHomePage from "./components/TheHomePage";
import TheInfoPage from "./components/TheInfoPage";
import FirstParallax from "./components/FirstParallax";
import TheProjectsPage from "./components/TheProjectsPage";
import TheAboutPage from "./components/TheAboutPage";

export default {
  name: "App",
  components: {
    NavigationDrawer,
    TheHomePage,
    TheInfoPage,
    FirstParallax,
    TheProjectsPage,
    TheAboutPage
  }
};
</script>

<style lang="scss">
html {
  scroll-behavior: smooth;
}
</style>
