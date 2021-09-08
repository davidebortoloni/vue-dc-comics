<template>
  <div id="app">
    <Header />
    <Content />
    <SecondarySection />
    <SecMenus />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Content from "./components/Content.vue";
import SecondarySection from "./components/SecondarySection.vue";
import SecMenus from "./components/SecMenus.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Content,
    SecondarySection,
    SecMenus,
    Footer,
  },
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
</style>
