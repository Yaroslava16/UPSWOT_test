<template>
  <div>
    <Header />
    <Hero />
    <Info :info="loginInfo" />
    <Footer />
  </div>
</template>

<script>
import Header from "~/components/header.vue";
import Hero from "~/components/hero.vue";
import Info from "~/components/loginInfo.vue";
import Footer from "~/components/footer.vue";
export default {
  data() {
    return {
      loginInfo: [
        {
          infoTitle: "Interactive Reporting",
          infoText:
            "In just a few clicks, you can connect your data from 1C, CRM (Bitrix24, AmoCRM, ZohoCRM), E-commerce (PROM.UA, Rozetka, ebay), Logistic (Nova Poshta), Google Analytics and many more systems that reflect different aspects of business activities.",
        },
        {
          infoTitle: "Automated data updates",
          infoText:
            "The application automatically updates and structures the data in just 60 seconds, saving you time and money.",
        },
        {
          infoTitle: "Data Security",
          infoText:
            "The Bank guarantees the safety of your personal data, ensuring their integrity and confidentiality.",
        },
      ],
    };
  },
  components: {
    Header,
    Hero,
    Info,
    Footer,
  },
};
</script>

<style lang="scss" scoped></style>
