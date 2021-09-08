<template>
  <footer>
    <div class="container">
      <div class="row justify-content-between">
        <div class="col h-100 d-flex align-items-center">
          <a href="#">
            <div class="btn">SIGN-UP NOW!</div>
          </a>
        </div>
        <div class="col h-100 d-flex align-items-center">
          <h2>FOLLOW US</h2>
          <ul>
            <li v-for="(icon, index) in socialIcons" :key="index">
              <div>
                <a href="#"
                  ><img :src="getIconUrl(icon.url)" :alt="icon.name"
                /></a>
              </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      socialIcons: [
        {
          name: "Facebook",
          url: "footer-facebook.png",
        },
        {
          name: "Twitter",
          url: "footer-twitter.png",
        },
        {
          name: "YouTube",
          url: "footer-youtube.png",
        },
        {
          name: "Pinterest",
          url: "footer-pinterest.png",
        },
        {
          name: "Periscope",
          url: "footer-periscope.png",
        },
      ],
    };
  },
  methods: {
    getIconUrl(url) {
      return require("@/assets/img/" + url);
    },
  },
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_vars.scss";

footer {
  font-family: "Roboto Condensed", sans-serif;
  background-color: #303030;
}
.row {
  height: 100px;
}
a {
  text-decoration: none;
  .btn {
    border: 3px solid $primaryColor;
    color: white;
    padding: 5px;
    &:hover {
      background-color: $primaryColor;
    }
  }
}
ul {
  list-style-type: none;
  display: inline-block;
  li {
    display: inline-block;
    margin: 0 15px;
  }
  a {
    display: inline-block;
    text-decoration: none;
    text-transform: uppercase;
    &:hover {
      color: $primaryColor;
    }
  }
}
h2 {
  display: inline-block;
  color: $primaryColor;
  margin-right: 15px;
}
</style>
