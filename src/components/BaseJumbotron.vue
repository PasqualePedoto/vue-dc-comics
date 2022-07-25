<template>
  <div id="jumbotron"></div>
</template>

<script>
export default {
  name: "BaseJumbotron",
};
</script>

<style scoped lang="scss">
#jumbotron {
  background-image: url("../assets/img/jumbotron.jpg");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;

  height: 700px;
  width: 100%;
}
</style>
