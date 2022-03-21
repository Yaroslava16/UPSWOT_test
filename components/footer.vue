<template>
  <div class="footer">
    <div class="footer__content">
      <img class="footer__logo" src="~/assets/logo.svg" alt="" />
      <ul class="footer__nav">
        <li class="footer__nav-item"><a>Terms & Conditions</a></li>
        <li class="footer__nav-item"><a>Privacy</a></li>
        <li class="footer__nav-item"><a>Notice at Collection</a></li>
        <li class="footer__nav-item"><a>CA Privacy Hub</a></li>
        <li class="footer__nav-item"><a>Contact Us</a></li>
        <li class="footer__nav-item"><a>Sitemap</a></li>
      </ul>
    </div>
    <div class="footer__copiright">
      Copyright © 2020 Citigroup Inc. Citibank, N.A. Member FDIC. Equal
      Opportunity Lender.
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.footer {
  justify-content: center;
  width: 100%;
  padding: 1.563vw 19.583vw;
  background-color: #333333;
  &__content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    padding-bottom: 1.589vw;
    margin-bottom: 1.589vw;
    a {
      font-weight: 500;
      font-size: 0.833vw;
      line-height: 156.69%;

      color: #fff;
    }

    border-bottom: 1px solid #fff;
  }
  &__logo {
    width: 2.917vw;
    height: 1.823vw;
    margin-left: 0.313vw;
  }
  &__nav {
    display: flex;
    &-item:not(:last-child) {
      margin-right: 1.042vw;
    }
  }
  &__copiright {
    font-weight: 500;
    font-size: 0.625vw;
    line-height: 156.69%;
    color: #fff;
  }
}
</style>
