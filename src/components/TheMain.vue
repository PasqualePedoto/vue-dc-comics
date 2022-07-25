<template>
  <main>
    <div id="content">
      <div class="container">
        <div>
          <ul>
            <li v-for="(comic, i) in comics" :key="i">
              <a href="#">
                <figure>
                  <img :src="comic.thumb" :alt="comic.series" />
                </figure>
                <p>{{ comic.series }}</p>
              </a>
            </li>
          </ul>
        </div>
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
export default {
  name: "TheMain",
  components: {},
  props: {
    ComicCards: Array,
  },
  data() {
    return {
      comics: [
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book",
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book",
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel",
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book",
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          price: "$3.99",
          series: "Batman",
          type: "comic book",
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book",
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book",
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book",
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book",
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book",
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book",
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel",
        },
      ],
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

    ul {
      display: flex;
      flex-wrap: wrap;
      width: 700px;

      margin: 0 auto;

      li {
        width: calc(100% / 6);
        border: 2px solid red;

        figure {
          width: 100%;
        }
      }
    }
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
