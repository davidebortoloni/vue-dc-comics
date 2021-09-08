<template>
  <div class="book">
    <div class="cover">
      <img :src="thumb" :alt="series" />
    </div>
    <h3>{{ series }}</h3>
  </div>
</template>

<script>
export default {
  name: "Book",
  props: ["thumb", "series"],
};
</script>

<style scoped lang="scss">
.book {
  width: 100%;
}
.cover {
  width: 100%;
  height: 150px;
  overflow: hidden;
  img {
    width: 100%;
  }
}
h3 {
  text-transform: uppercase;
  color: white;
  font-size: 14px;
  margin-top: 15px;
}
</style>
