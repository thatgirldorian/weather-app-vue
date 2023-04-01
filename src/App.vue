<template>
  <div>
    <NavigationBar />
    <RouterView />
  </div>
</template>

<script setup>
import {RouterView} from "vue-router"
import NavigationBar from "./components/NavigationBar.vue"
</script>

<style lang="css" scoped>

</style>