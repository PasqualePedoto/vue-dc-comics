<template>
  <footer>
    <TheTopFooter />
    <TheBottomFooter />
  </footer>
</template>

<script>
import TheTopFooter from "./TheTopFooter.vue";
import TheBottomFooter from "./TheBottomFooter.vue";

export default {
  name: "TheFooter",
  components: {
    TheTopFooter,
    TheBottomFooter,
  },
};
</script>

<style lang="scss" scoped>
footer {
  flex-grow: 1;

  background-image: url("../assets/img/footer-bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}
</style>
