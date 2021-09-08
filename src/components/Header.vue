<template>
  <header class="container">
    <div class="row justify-content-between align-items-center">
      <div class="col h-100">
        <img src="@/assets/img/dc-logo.png" alt="DC-logo" class="h-100" />
      </div>
      <div class="col h-100">
        <ul class="h-100">
          <li
            v-for="(link, index) in links"
            :key="index"
            class="h-100"
            :class="{ active: link.current }"
          >
            <div class="h-100 d-flex align-items-center">
              <a class="text-grey text-small" :href="link.url">{{
                link.text
              }}</a>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      links: [
        {
          text: "Characters",
          url: "#",
          current: false,
        },
        {
          text: "Comics",
          url: "#",
          current: true,
        },
        {
          text: "Movies",
          url: "#",
          current: false,
        },
        {
          text: "TV",
          url: "#",
          current: false,
        },
        {
          text: "Games",
          url: "#",
          current: false,
        },
        {
          text: "Collectibles",
          url: "#",
          current: false,
        },
        {
          text: "Videos",
          url: "#",
          current: false,
        },
        {
          text: "Fans",
          url: "#",
          current: false,
        },
        {
          text: "News",
          url: "#",
          current: false,
        },
        {
          text: "Shop",
          url: "#",
          current: false,
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
header {
  font-family: "Roboto Condensed", sans-serif;
}
.row {
  height: 85px;
}
ul {
  list-style-type: none;
  li {
    display: inline-block;
    margin: 0 15px;
    padding: 2px 0;
    &.active div {
      border-bottom: 4px solid #0282f9;
      a {
        color: #0282f9;
      }
    }
  }
  a {
    display: inline-block;
    text-decoration: none;
    text-transform: uppercase;
    &:hover {
      color: #0282f9;
    }
  }
}
img {
  padding: 12px;
}
</style>
