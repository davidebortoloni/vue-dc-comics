<template>
  <div class="menu">
    <h3 class="text-white">{{ menu.title }}</h3>
    <ul>
      <li v-for="(item, index) in menu.items" :key="index">
        <a class="text-lightgrey text-small" href="#">{{ item }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "SecMenu",
  props: ["menu"],
};
</script>

<style scoped lang="scss">
.menu {
  font-family: "Roboto Condensed", sans-serif;
  padding: 10px 0;
}
h3 {
  margin-top: 10px;
  text-transform: uppercase;
}
ul {
  list-style-type: none;
  a {
    text-decoration: none;
    &:hover {
      color: white;
    }
  }
}
</style>
