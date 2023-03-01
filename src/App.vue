<script>
import headerApp from "./components/headerApp.vue";
import mainApp from "./components/mainApp.vue";

export default {
  components: { headerApp, mainApp },
};
</script>
<template>
  <headerApp />

  <mainApp />
</template>
<style lang="scss">
@use "./assets/scss/style.scss" as *;
</style>
