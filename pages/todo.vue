<template>
  <div class="todo">
    <div class="todo__top-part">
      <img class="todo__logo" src="~/assets/logo.svg" alt="" />
    </div>
    <div class="todo__bottom-part"></div>
    <div class="todo__content">
      <p class="todo__content-title">Thank you ${name}!</p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.todo {
  width: 100%;
  position: relative;
  &__logo {
    margin: 0 auto;

    width: 9.688vw;
    height: 6.198vw;
  }
  &__top-part {
    padding-top: 3.385vw;
    height: 41.51vw;
    background: linear-gradient(180deg, #00afed 0%, #00569a 100%);
  }
  &__bottom-part {
    min-height: 14.74vw;
    background: #e5e5e5;
  }
  &__content {
    position: absolute;
    top: 58.6%;
    left: 50%;
    transform: translate(-50%, -50%);

    width: 62.031vw;
    height: 40vw;
    padding: 1.667vw 0;
    background-color: #fff;

    &-title {
      font-weight: 700;
      font-size: 3.125vw;
      line-height: 156.69%;

      text-align: center;
    }
  }
}
</style>
