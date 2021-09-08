<template>
  <section class="d-flex align-items-center">
    <div class="container">
      <div class="row h-100">
        <div class="col">
          <SecMenu :menu="menus[0]" />
          <SecMenu :menu="menus[1]" />
        </div>
        <div class="col">
          <SecMenu :menu="menus[2]" />
        </div>
        <div class="col">
          <SecMenu :menu="menus[3]" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import SecMenu from "./SecMenu.vue";
export default {
  components: { SecMenu },
  name: "SecMenus",
  data() {
    return {
      menus: [
        {
          title: "DC Comics",
          items: [
            "Characters",
            "Comics",
            "Movies",
            "TV",
            "Games",
            "Videos",
            "News",
          ],
        },
        {
          title: "Shop",
          items: ["Shop DC", "Shop DC Collectibles"],
        },
        {
          title: "DC",
          items: [
            "Terms Of Use",
            "Privacy policy (New)",
            "Ad Choices",
            "Advertising",
            "Jobs",
            "Subscriptions",
            "Talent Workshops",
            "CPSC Certificates",
            "Ratings",
            "Shop Help",
            "Contact Us",
          ],
        },
        {
          title: "Sites",
          items: [
            "DC",
            "MAD Magazine",
            "DC Kids",
            "DC Universe",
            "DC Power Visa",
          ],
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_mixin.scss";
section {
  height: 350px;
  background-image: url("../assets/img/footer-bg.jpg");
  background-size: cover;
}
.container {
  flex-basis: 1200px;
}
.col {
  flex-basis: 150px;
}
</style>
