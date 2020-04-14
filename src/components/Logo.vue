<template>
  <div class="logo-box">
    <div class="logo-box__image">
      <img src="@/assets/images/logo.svg" alt="logo" />
    </div>
    <div class="logo-box__text">
      <h3>APOLLO 13</h3>
      <h4>"Houston, we have a problem."</h4>
    </div>
  </div>
</template>

<script>
export default {
  name: "Logo"
};
</script>

<style lang="scss" scoped>
.logo-box {
  display: grid;
  grid-template-columns: 65px 1fr;
  grid-template-rows: fill;
  column-gap: 15px;
  width: 100%;
  // height: 80px;
  // display: inline-block;

  // overflow: hidden;
  &__image {
    align-self: center;
    // margin: 0;
    // display: inline-block;
    position: relative;
    img {
      margin-top: 5px;
      align-self: center;
      // display: block;
      // width: 100%;
      // height: 100%;
      // position: absolute;
      // top: 0;
    }
  }
}
.logo-box__text {
  color: #202020;
  h3 {
    font-family: Ultra;
    font-size: 3.5rem;
  }

  h4 {
    font-family: Anton;
    font-size: 2.0rem;
  }
}
</style>
