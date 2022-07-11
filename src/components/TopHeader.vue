<template>
  <header>
    <img src="../assets/logo-small.svg" alt="logo spotify" />
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
  display: flex;
  align-items: center;
  padding: 0.5rem;
}
img {
  max-height: 80%;
}
</style>
