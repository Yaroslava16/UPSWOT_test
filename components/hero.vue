<template>
  <div class="hero">
    <p class="hero__title">
      Welcome to<br />
      Business Analytics Online
    </p>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.hero {
  display: inline-flex;
  align-items: flex-end;
  width: 100%;
  height: 23.802vw;
  padding: 0 0 3.646vw 19.323vw;
  background-image: url(~/assets/hero_img.png);
  background-repeat: no-repeat;
  background-size: cover;
  &__title {
    width: 32.76vw;
    font-weight: 400;
    font-size: 2.865vw;
    line-height: 156.69%;
    color: #fff;
  }
}
</style>
