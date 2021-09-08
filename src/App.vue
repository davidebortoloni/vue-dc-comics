<template>
  <div id="app">
    <Header />
    <Content />
    <SecondarySection />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Content from "./components/Content.vue";
import SecondarySection from "./components/SecondarySection.vue";

export default {
  name: "App",
  components: {
    Header,
    Content,
    SecondarySection,
  },
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
</style>
