<template>
  <div class="header">
    <div class="header__top-part"></div>
    <div class="header__bottom-part">
      <img class="header__logo" src="~/assets/logo.svg" alt="" />
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.header {
  &__top-part {
    width: 100%;
    height: 2.76vw;
    background-color: #333333;
  }
  &__bottom-part {
    display: flex;
    align-items: center;
    width: 100%;
    height: 5vw;
    background: linear-gradient(180deg, #00afed 0%, #00569a 100%);
  }
  &__logo {
    width: 5.365vw;
    height: 3.438vw;
    margin-left: 19.635vw;
  }
}
</style>
