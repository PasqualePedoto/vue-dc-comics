<template>
  <footer>
    <TheTopFooter />
  </footer>
</template>

<script>
import TheTopFooter from "./TheTopFooter.vue";

export default {
  name: "TheFooter",
  components: {
    TheTopFooter,
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
