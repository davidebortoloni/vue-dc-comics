<template>
  <section>
    <div class="container">
      <div class="row">
        <div class="col h-100 text-white text-medium">
          --> Content goes here &#60;--
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Content",
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_mixin.scss";
section {
  font-family: "Roboto Condensed", sans-serif;
  background-color: black;
}
.row {
  height: 100px;
  .col {
    @include center("vertical");
  }
}
</style>
