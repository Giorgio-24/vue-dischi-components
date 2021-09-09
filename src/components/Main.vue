<template>
  <main class="container">
    <section class="row">
      <div
        class="card col-2 text-center"
        v-for="(album, index) in albums"
        :key="index"
      >
        <Card :album="album" />
      </div>
    </section>
  </main>
</template>

<script>
import axios from "axios";
import Card from "./Card.vue";
export default {
  name: "Main",
  components: {
    Card,
  },
  data() {
    return {
      albums: {},
    };
  },
  created() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((res) => {
        this.albums = res.data.response;
      })
      .catch((err) => {
        console.log(err);
      });
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_vars.scss";
section .card {
  background-color: $dark-blue;
  padding: 20px;
  margin: 20px;
  flex-basis: 220px;
  min-height: 350px;
}
</style>