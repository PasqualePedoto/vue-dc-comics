<template>
  <main>
    <div id="content">
      <div class="container">
        <ComicCardsSection :comic-cards="ComicCards" />
      </div>
    </div>
    <div id="merch">
      <div class="container">
        <ul>
          <li v-for="link in merchLinks" :key="link.src">
            <a :href="link.href">
              <figure>
                <img :src="link.src" :alt="link.alt" />
              </figure>
            </a>
            <p>{{ link.alt }}</p>
          </li>
        </ul>
      </div>
    </div>
  </main>
</template>

<script>
import ComicCardsSection from "./ComicCardsSection.vue";
export default {
  name: "TheMain",
  components: { ComicCardsSection },
  props: {
    ComicCards: Array,
  },
  data() {
    return {
      merchLinks: [
        {
          src: `${require("../assets/img/buy-comics-digital-comics.png")}`,
          alt: "DIGITAL COMICS",
          href: "#",
        },
        {
          src: `${require("../assets/img/buy-comics-merchandise.png")}`,
          alt: "COMICS MERCHANDIZING",
          href: "#",
        },
        {
          src: `${require("../assets/img/buy-comics-shop-locator.png")}`,
          alt: "SHOP LOCATOR",
          href: "#",
        },
        {
          src: `${require("../assets/img/buy-comics-subscriptions.png")}`,
          alt: "COMICS SUBSCRIPTIONS",
          href: "#",
        },
        {
          src: `${require("../assets/img/buy-dc-power-visa.svg")}`,
          alt: "POWER VISA",
          href: "#",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
main {
  flex-shrink: 0;

  #content {
    padding: 50px;
    background-color: black;

    position: relative;
  }

  #merch {
    position: absolute;
    right: 0;
    left: 0;
    z-index: 3;

    background-color: #1c82f9;
    height: 100px;

    .container {
      height: 100%;

      ul {
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        height: 100%;

        li {
          height: 100%;

          min-width: 50px;
          height: 50px;

          display: flex;
          align-items: center;
          justify-content: center;

          p {
            margin-left: 10px;

            color: white;
          }

          figure {
            width: 50px;
            height: 50px;
          }
        }
      }
    }
  }
}
</style>
