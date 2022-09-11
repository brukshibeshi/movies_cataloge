<template>
  <div>
    <v-app-bar flat color="rgba(0, 0, 0, 0.1)" absolute>
      <v-img contain height="50" width="150" :src="logo" class="w-logo"></v-img>

      <v-spacer></v-spacer>
      <template v-for="(menu, i) in menus">
        <a :key="i" :href="menu.link" class="w-menu-item">{{ menu.name }}</a>
      </template>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-menu left bottom class="mx-4">
        <template v-slot:activator="{ on, attrs }">
          <v-row class="mx-auto" v-bind="attrs" v-on="on">
            <v-list-item-avatar>
              <v-img :src="userInfo.avatar"></v-img>
            </v-list-item-avatar>
            <v-list-item-content>
              <v-list-item-title class="text-h6">{{ userInfo.name }}</v-list-item-title>
            </v-list-item-content>
          </v-row>
        </template>

        <v-list>
          <v-list-item v-for="n in 5" :key="n" @click="() => {}">
            <v-list-item-title>Option {{ n }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  data() {
    return {
      logo: require("@/assets/imgs/logo2.png"),
      userInfo: {
        avatar: "https://cdn.vuetifyjs.com/images/john.png",
        name: "Abebe Balcha",
      },
      menus: [
        {
          name: "Home",
          link: "/",
        },
        {
          name: "Movies",
          link: "/movies",
        },
        {
          name: "TV Show",
          link: "/tv_shows",
        },
        {
          name: "Video",
          link: "/videos",
        },
        {
          name: "FAQ",
          link: "/faqs",
        },
        {
          name: "Pricing",
          link: "/pricing",
        },
        {
          name: "Contact Us",
          link: "/contact_us",
        },
      ],
    };
  },
};
</script>

<style>
.w-menu-item {
  margin-left: 10px;
  margin-right: 10px;
}
.w-logo{
  background: rgba(51, 79, 108, 0.973);
}
</style>
