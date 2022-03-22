<template>
  <div class="info">
    <p class="info__title">
      <b>Business Analytics</b> — a new, convenient tool for managing and
      forecasting your business performance, which will help analyze your own
      finances and cash flows, visualize your reporting, business processes,
      KPI's
    </p>
    <ul class="info__list">
      <li class="info__item" v-for="(item, i) in info" :key="i">
        <span class="info__item-title"
          ><img class="info__item-icon" src="~/assets/info_icon.svg" alt="" />{{
            item.infoTitle
          }}</span
        >
        <p class="info__item-text">{{ item.infoText }}</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    info: [],
  },
};
</script>

<style lang="scss" scoped>
.info {
  width: 54.72vw;
  padding: 2.083vw 0 2.083vw 19.323vw;
  :not(:last-child) {
    margin-bottom: 0.781vw;
  }
  &__title {
    margin-bottom: 0.781vw;
    font-weight: 400;
    font-size: 0.833vw;
    line-height: 156.69%;
  }
  &__item {
    &-icon {
      width: 1.198vw;
      height: 0.885vw;
      margin-right: 0.781vw;
    }
    &-title {
      display: flex;
      align-items: center;
      margin-bottom: 0.521vw;

      font-weight: 500;
      font-size: 0.833vw;
      line-height: 156.69%;
    }
    &-text {
      margin-left: 1.979vw;

      font-weight: 400;
      font-size: 0.729vw;
      line-height: 156.69%;
    }
  }
}
</style>
