<template>
  <header>
    <div class="container">
      <img src="../assets/img/logo.png" alt="" />
      <select>
        <option value="All" selected>All</option>
        <option></option>
      </select>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/_vars.scss";
header {
  background-color: $dark-blue;
  height: 70px;
  padding: 10px;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  & > div.container {
    display: flex;
    justify-content: space-between;
    img {
      height: 50px;
    }
    select {
      height: 20px;
      align-self: flex-end;
    }
  }
}
</style>