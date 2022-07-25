<template>
  <div>
    <ul>
      <li v-for="(comic, i) in ComicCards" :key="i">
        <a href="#">
          <figure>
            <img :src="comic.thumb" :alt="comic.series" />
          </figure>
          <p>{{ comic.series }}</p>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "ComicCardsSection",
  props: {
    ComicCards: Array,
  },
};
</script>

<style lang="scss" scoped>
ul {
  display: flex;
  flex-wrap: wrap;
  width: 700px;

  margin: 0 auto;

  li {
    width: calc(100% / 6);
    border: 2px solid #1c82f9;

    figure {
      width: 100%;
    }
  }
}
</style>
