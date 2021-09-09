<template>
  <div>
    <img class="img-fluid" :src="album.poster" alt="New Jersey" />
    <h4 class="text-light h6 my-3 fw-bold text-uppercase">{{ album.title }}</h4>
    <address class="mb-0">{{ album.author }}</address>
    <time :datetime="album.year">{{ album.year }}</time>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ["album"],
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_vars.scss";
address,
time {
  color: $grey;
}
</style>