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
    <BlueFlag blue-flag-text="LOAD MORE" />
  </div>
</template>

<script>
import BlueFlag from "./BlueFlag.vue";

export default {
  name: "ComicCardsSection",
  components: {
    BlueFlag,
  },
  props: {
    ComicCards: Array,
  },
};
</script>

<style lang="scss" scoped>
ul {
  display: flex;
  flex-wrap: wrap;
  width: 80%;

  margin: 0 auto;

  li {
    width: calc(100% / 6 - 20px);
    border: 2px solid #1c82f9;
    margin: 10px 10px;

    figure {
      width: 100%;
    }
  }
}
</style>
