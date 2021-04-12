<template>
  <div>
    <v-navigation-drawer
      v-model="drawer"
      :color="black"
      app
      clipped
      dark
      temporary
      class="py-1"
    >
      <v-list-item>
        <v-list-item-title class="title">
          Back
        </v-list-item-title>
        <v-btn icon>
          <v-icon>mdi-chevron-left</v-icon>
        </v-btn>
      </v-list-item>
      <v-divider></v-divider>
      <v-list dense nav class="py-2">
        <v-list-item v-for="item in items" :key="item.title" link class="py-3">
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar app clipped-left>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title id="toolbar_title">TyL's Portfolio</v-toolbar-title>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  name: "ToolBar",

  data: () => ({
    drawer: null,
    items: [
      { title: "Home", icon: "mdi-home", path: "/" },
      { title: "About", icon: "mdi-information", path: "/about" },
      { title: "Skill", icon: "mdi-laptop", path: "/skill" },
      { title: "Blog", icon: "mdi-post", path: "/blog" },
      { title: "Contact", icon: "mdi-account-box", path: "/contact" }
    ]
  })
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Economica:700");
#toolbar_title {
  /* Google fontsで導入したいfontsからfont-familyを取ってくる */
  font-family: "Economica", sans-serif;
  font-size: 26px;
}
</style>