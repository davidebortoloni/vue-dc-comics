<template>
  <div id="app">
    <Header />
  </div>
</template>

<script>
import Header from "./components/Header.vue";

export default {
  name: "App",
  components: {
    Header,
  },
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.container {
  max-width: 1200px;
  margin: 0 auto;
}
.d-flex {
  display: flex;
}
.row {
  display: flex;
  flex-direction: row;
}
.h-100 {
  height: 100%;
}
.justify-content-between {
  justify-content: space-between;
}
.align-items-center {
  align-items: center;
}
.text-grey {
  color: rgb(46, 46, 46);
}
.text-small {
  font-size: 13px;
}
</style>
