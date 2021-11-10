<template>
  <div>
    <TheHeader @sidenavToggle="displaySideNav = !displaySideNav" />
    <TheSideNav :show="displaySideNav" @close="displaySideNav = false" />
    <nuxt />
  </div>
</template>

<script>
import { ref } from "@vue/composition-api";

import TheHeader from "@/components/Navigation/TheHeader.vue";
import TheSideNav from "@/components/Navigation/TheSidenav.vue";

export default {
  components: {
    TheHeader,
    TheSideNav,
  },
  setup(){
    const displaySideNav = ref(false);
    
    return {displaySideNav};
  },

};
</script>

<style>
html {
  font-family: "Open Sans", sans-serif;
}
body {
  margin: 0;
}
</style>