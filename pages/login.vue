<template>
  <div>
    <Header />
    <Hero />
    <Footer />
  </div>
</template>

<script>
import Header from "~/components/header.vue";
import Hero from "~/components/hero.vue";
import Footer from "~/components/footer.vue";
export default {
  components: {
    Header,
    Hero,
    Footer,
  },
};
</script>

<style lang="scss" scoped></style>
