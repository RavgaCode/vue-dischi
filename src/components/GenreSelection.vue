<template>
  <div class="selection-bar text-center">
    <select
      name="genre-select"
      id="genre-select"
      @change="$emit('genreChanged', genreToFilter)"
      v-model="genreToFilter"
    >
      <option value="all">All</option>
      <option value="rock">Rock</option>
      <option value="pop">Pop</option>
      <option value="jazz">Jazz</option>
      <option value="metal">Metal</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "GenreSelection",
  data() {
    return {
      genreToFilter: "all",
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";
</style>
