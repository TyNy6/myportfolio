<template>
  <div class="bg-video-wrap">
    <video src="@/assets/Lines.mp4" loop muted autoplay></video>
    <div class="overlay"></div>
  </div>
</template>
<script>
export default {
  name: "BackGround",
  created() {
    this.$vuetify.theme.dark = true;
  }
};
</script>
<style scoped>
.bg-video-wrap {
  object-fit: cover;
  position: fixed;
  overflow: hidden;
  width: 100%;
  height: 100%;
}
video {
  object-fit: cover;
  position: fixed;
  min-width: 100%;
  min-height: 100%;
  z-index: 1;
}
.overlay {
  background-color: rgba(0, 0, 0, 0.6);
  width: 100%;
  height: 100%;
  position: fixed;
  top: 0;
  left: 0;
  background-size: 4px 4px;
  z-index: 2;
}
</style>