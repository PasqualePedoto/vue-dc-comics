<template>
  <div id="blue-flag">
    <p>{{ BlueFlagText }}</p>
  </div>
</template>

<script>
export default {
  name: "BlueFlag",
  props: {
    BlueFlagText: String,
  },
};
</script>

<style scoped lang="scss">
#blue-flag {
  background-color: #1c82f9;
  color: white;
  padding: 0.5rem;
  text-align: center;
  margin: 0 auto;

  width: 150px;
}
</style>
