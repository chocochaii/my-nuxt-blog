<template>
  <div>
    <TheHeader @sidenavToggle="displaySidenav = !displaySidenav" />
    <TheSidenav
      :show="displaySidenav"
      @close="displaySidenav = false" />
    <nuxt/>
  </div>
</template>

<script>
import TheHeader from "@/components/navigation/TheHeader";
import TheSidenav from "@/components/navigation/TheSidenav";

export default {
  components: {
    TheHeader,
    TheSidenav
  },
  data() {
    return {
      displaySidenav: false
    };
  }
};
</script>


<style lang="scss">
* {
  box-sizing: border-box;
}
html {
  font-family: "Open Sans", sans-serif;
}
body {
  margin: 0;
}
h1,
h2,
h3,
h4,
h5,
h6,
p,
ul,
li,
span,
a,
textarea,
input,
div {
  color: #222222;
}
a {
  text-decoration: none;
}
</style>
