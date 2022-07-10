<template>
  <header>
    <img src="../assets/logo-spotify.jpg" alt="logo spotify" />
  </header>
</template>

<script>
export default {
  name: "TopHeader",
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";

header {
  background-color: $light-color;
  height: 100px;
}
img {
  max-height: 100%;
}
</style>
