<script setup>
import Registration from "./components/Registration.vue";
</script>

<template>
  <Registration />
</template>

<style lang="scss">
@import "./styles/_global.scss";

#app {
  @include flex-row;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 100%;
}
</style>
