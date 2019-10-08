<template>
  <v-container class="pa-4" id="info">
    <h2 class="mt-4" justify="start">Info</h2>
    <v-row class="fill-height" align="center" justify="center">
      <template v-for="(item, i) in items">
        <v-col :key="i" cols="12" md="3">
          <v-hover v-slot:default="{ hover }">
            <v-card :elevation="hover ? 12 : 2" :class="{ 'on-hover': hover }">
              <v-img :src="'/img/'+item.img" height="300px">
                <v-card-title class="title white--text">
                  <v-row class="fill-height flex-column" justify="space-between">
                    <p class="ml-4 mt-4 subheading text-left">{{ item.title }}</p>

                    <div>
                      <p
                        class="ml-4 ma-0 body-1 font-italic text-left"
                        v-for="value in item.list"
                        :key="value"
                      >{{ value }}</p>
                      <p class="caption font-weight-medium font-italic text-left">{{ item.subtext }}</p>
                    </div>
                  </v-row>
                </v-card-title>
              </v-img>
            </v-card>
          </v-hover>
        </v-col>
      </template>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "TheInfoPage",
  data: () => ({
    items: [
      {
        title: " Front-End",
        list: {
          1: "React",
          2: "Vue",
          3: "Javascript",
          4: "HTML + CSS",
          5: "scss"
        },
        img: "front-end.jpg"
      },
      {
        title: " Back-End",
        list: {
          1: "PHP",
          2: "Node.js",
          3: "MySQL",
          4: "Rest API",
          5: "docker"
        },
        img: "back-end.jpg"
      },
      {
        title: " Design",
        list: {
          1: "Photoshop",
          2: "Illustrator",
          3: "InDesign",
          4: "figma",
          5: "sketch"
        },
        img: "design.jpg"
      },
      {
        title: " Language",
        list: {
          1: "Cantonese",
          2: "Dutch",
          3: "English",
          4: "French",
          5: "Mandarin"
        },
        img: "language.jpg"
      },
      {
        title: " Education",
        list: {
          1: "AP Hogeschool: Chemie",
          2: "VDAB: Prepress",
          3: "BeCode: Junior Web Developer",
          4: "Driver Licence: B"
        },
        img: "education.jpg"
      },
      {
        title: " Experience",
        list: {
          1: "2007-2009: Umicore Lab Technician",
          2: "2010: JPG Pharma Desktop Publisher",
          3: "2011-2019: Gazelle Prepress Coordinator"
        },
        img: "experience.jpg"
      },
      {
        title: " Hobbies",
        list: {
          1: "Gaming",
          2: "D&D",
          3: "Reading",
          4: "Comics",
          5: "Music"
        },
        img: "hobbies.jpg"
      },
      {
        title: " Contact",
        list: {
          1: "Grote Markt 50, 2000 Antwerpen",
          2: "+32 (0) 485 47 41 48",
          3: "cheungkin.wong@gmail.com"
        },
        img: "contact.jpg"
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