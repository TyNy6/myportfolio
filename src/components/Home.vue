<template>
  <v-container fluid fill-height>
    <v-row justify="center" align="center">
      <vue-typer text="Welcome to My Portfolio"></vue-typer>
    </v-row>
  </v-container>
</template>

<script>
export default {};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Economica:700");
.vue-typer {
  font-family: "Economica", sans-serif;
  font-size: 96px;
  z-index: 3;
}
.vue-typer .custom.char.typed {
  color: #ffffff;
}
.vue-typer .custom.char.selected {
  color: #ffffff;
  background-color: transparent;
  text-decoration: line-through;
}
</style>
