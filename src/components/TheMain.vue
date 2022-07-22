<template>
  <main>
    <div class="container">
      <h2>Content is here</h2>
    </div>
  </main>
</template>

<script>
export default {
  name: "TheMain",
};
</script>

<style lang="scss" scoped>
main {
  padding: 50px;
  background-color: black;
  flex-shrink: 0;

  h2 {
    font-weight: bold;
    color: white;
  }
}
</style>
