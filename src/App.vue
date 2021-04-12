<template>
  <v-app dark>
    <v-content>
      <BackGround />
      <ToolBar />
      <Home />
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: "App",

  components: {
    BackGround: () => import("@/components/BackGround"),
    ToolBar: () => import("@/components/ToolBar"),
    Home: () => import("@/components/Home")
  },

  data: () => ({
    //
  })
};
</script>
<style >
</style>