<template>
  <main>
    <div class="grid">
      <div class="row">
        <div
          class="col-12 col-md-6 col-lg-3 my-5"
          v-for="(album, index) in albumList"
          :key="index"
        >
          <div class="text-center album-card">
            <img :src="album.poster" :alt="album.title" />
            <h3>{{ album.title }}</h3>
            <h5>{{ album.author }}</h5>
            <h5>{{ album.year }}</h5>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import axios from "axios";
export default {
  name: "MainContent",
  data() {
    return {
      url: "https://flynn.boolean.careers/exercises/api/array/music",
      albumList: [],
    };
  },
  created() {
    this.getAlbum();
  },
  methods: {
    getAlbum() {
      axios
        .get(this.url)
        .then((response) => {
          this.albumList = response.data.response;
        })
        .catch((err) => {
          console.log("Error", err);
        });
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";
main {
  background-color: $dark-color;
  color: white;
}
.grid {
  width: 80%;
  margin: 0 auto;
}
.album-card {
  background-color: $light-color;
  padding-top: 2rem;
  padding-inline: 1rem;
  height: 600px;
}
img {
  max-width: 100%;
}
h5 {
  color: lightgray;
}
</style>
