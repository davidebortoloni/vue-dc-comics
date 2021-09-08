<template>
  <section>
    <div class="container">
      <div class="row">
        <div class="col h-100">
          <ul class="h-100">
            <li v-for="(icon, index) in icons" :key="index" class="h-100">
              <img class="h-100" :src="getImgUrl(icon.url)" :alt="icon.text" />
              <div class="text-white text-small">{{ icon.text }}</div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "SecondarySection",
  data() {
    return {
      icons: [
        {
          text: "Digital Comics",
          url: "buy-comics-digital-comics.png",
        },
        {
          text: "DC Merchandise",
          url: "buy-comics-merchandise.png",
        },
        {
          text: "Subscrition",
          url: "buy-comics-subscriptions.png",
        },
        {
          text: "Comic Shop Locator",
          url: "buy-comics-shop-locator.png",
        },
        {
          text: "DC Power Visa",
          url: "buy-dc-power-visa.svg",
        },
      ],
    };
  },
  methods: {
    getImgUrl(url) {
      return require("@/assets/img/" + url);
    },
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";
@import "../assets/scss/_mixin.scss";
section {
  background-color: $primaryColor;
  font-family: "Roboto Condensed", sans-serif;
}
.row {
  height: 130px;
  @include center();
  padding: 40px;
}
ul {
  list-style-type: none;
  @include center();
  li {
    display: inline-block;
    margin: 0 30px;
    text-transform: uppercase;
    @include center();
    img {
      margin: 0 15px;
    }
  }
}
</style>
