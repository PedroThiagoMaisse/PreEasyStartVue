<template>
  <v-container class="pa-0 ma-0">
    <v-row class="text-center pa-0 ma-0 screen">
      <div class="banner">
        <v-col cols="12">
          <v-img
            :src="require('../assets/logo.svg')"
            class="my-3"
            contain
            height="200"
          />
        </v-col>

        <v-col class="mb-4">
          <h1 class="display-2 font-weight-bold mb-3">
            EasyStart - Vue + Vuetify + Heroku
          </h1>

          <p class="subheading font-weight-regular">
            For any help read this project README, and refeer to each parts
            documentation
          </p>
        </v-col>
      </div>

      <v-col class="mb-5" cols="12" v-for="i in viewlinks" :key="i.name">
        <h2 class="headline font-weight-bold mb-3">{{ i.name }}</h2>

        <v-row justify="center">
          <a
            v-for="o in i.list"
            :key="o"
            :href="o.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ o.text }}
          </a>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",

  data: () => ({
    viewlinks: [
      {
        name: "Ecosystem",
        list: [
          {
            text: "vuetify-loader",
            href: "https://github.com/vuetifyjs/vuetify-loader",
          },
          {
            text: "github",
            href: "https://github.com/vuetifyjs/vuetify",
          },
          {
            text: "awesome-vuetify",
            href: "https://github.com/vuetifyjs/awesome-vuetify",
          },
        ],
      },
      {
        name: "Important Links",
        list: [
          {
            text: "Documentation",
            href: "https://vuetifyjs.com",
          },
          {
            text: "Chat",
            href: "https://community.vuetifyjs.com",
          },
          {
            text: "Made with Vuetify",
            href: "https://madewithvuejs.com/vuetify",
          },
          {
            text: "Twitter",
            href: "https://twitter.com/vuetifyjs",
          },
          {
            text: "Articles",
            href: "https://medium.com/vuetify",
          },
        ],
      },
      {
        name: "What's next?",
        list: [
          {
            text: "Explore components",
            href: "https://vuetifyjs.com/components/api-explorer",
          },
          {
            text: "Select a layout",
            href: "https://vuetifyjs.com/getting-started/pre-made-layouts",
          },
          {
            text: "Frequently Asked Questions",
            href: "https://vuetifyjs.com/getting-started/frequently-asked-questions",
          },
        ],
      },
    ],
  }),
};
</script>

<style scoped>
.banner {
  width: 100vw;
  background-color: #4e6173;
}

.screen {
  width: 100vw;
}
</style>
