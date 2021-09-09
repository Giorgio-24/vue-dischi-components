<template>
  <header>
    <div class="container">
      <img src="" alt="" />
      <select>
        <option value="All" selected>All</option>
        <option></option>
      </select>
    </div>
  </header>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
/* @import "/scss/_vars.scss"; */
header {
  /*   background-color: $dark-blue; */
  height: 70px;
  padding: 10px;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
}

header > div.container {
  display: flex;
  justify-content: space-between;
}

header > div.container select {
  height: 20px;
  align-self: flex-end;
}

header img {
  height: 50px;
}
</style>