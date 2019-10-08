<template>
  <v-container class="pa-4" id="projects">
    <h2 class="header mt-4">Projects</h2>

    <v-row class="fill-height" align="center" justify="center">
      <template v-for="(item, i) in items">
        <v-col :key="i" cols="12" md="3">
          <v-hover v-slot:default="{ hover }">
            <v-card class="mx-auto" :elevation="hover ? 12 : 2" :class="{ 'on-hover': hover }">
              <v-img :src="'/img/'+item.img" height="200px"></v-img>
              <v-card-title class="d-bloc flex-column">
                <div>{{ item.title }}</div>
                <span class="grey--text subtitle-1">{{item.summary}}</span>
              </v-card-title>
              <v-card-actions>
                <v-btn text :href="item.preview" target="_blank">Preview</v-btn>
                <v-btn text color="blue-grey " :href="item.github" target="_blank">Github</v-btn>
                <div class="flex-grow-1"></div>
                <v-btn icon @click="item.show = !item.show">
                  <v-icon>{{ item.show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
                </v-btn>
              </v-card-actions>

              <v-expand-transition>
                <div v-show="item.show">
                  <v-card-text>{{item.text}}</v-card-text>
                </div>
              </v-expand-transition>
            </v-card>
          </v-hover>
        </v-col>
      </template>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "TheProjectsPage",
  data: () => ({
    items: [
      {
        title: "Memory game",
        summary: "Find all the pairs",
        text:
          "It's playable by keyboard and mouse and has local multiplayer. The project challenged my knowledge of HTML, CSS and JS.",
        img: "back.jpg",
        preview: "https://cheungkinwong.github.io/Memory-game/",
        github: "https://github.com/cheungkinwong/Memory-game/",
        show: false
      },
      {
        title: "Weather App",
        summary: "Weather forecast",
        text:
          "Excercise using Rest API, enter a city name and get the weather forecast for the next five days. Figuring out how to request and use data from an API took a while.",
        img: "10d.jpg",
        preview: "https://cheungkinwong.github.io/weather-app/",
        github: "https://github.com/cheungkinwong/weather-app/",
        show: false
      },
      {
        title: "Project Eden",
        summary: "Fictional project",
        text:
          "A group project to make a 1 page website for a fictional project. I was responsible for the navbar and making sure there were no merge conflicts.",
        img: "city1.jpg",
        preview: "https://cheungkinwong.github.io/project-eden/",
        github: "https://github.com/cheungkinwong/project-eden/",
        show: false
      },
      {
        title: "The world",
        summary: "3D world globe",
        text:
          "Introduction project to three.js full 3D controls, with both keyboard and mouse. First time doing 3D animation was Challenging.",
        img: "earthmap1k.jpg",
        preview: "https://cheungkinwong.github.io/threejs-The-World/",
        github: "https://github.com/cheungkinwong/threejs-The-World/",
        show: false
      }
    ],
    transparent: "rgba(255, 255, 255, 0)"
  })
};
</script>

<style lang="scss" scoped>
li {
  list-style: none;
}
.v-card {
  transition: opacity 0.4s ease-in-out;
}

.v-card:not(.on-hover) {
  opacity: 0.6;
}

.show-btns {
  color: rgba(255, 255, 255, 1) !important;
}
</style>