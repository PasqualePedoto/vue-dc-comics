<template>
  <div class="container">
    <div id="top-footer">
      <!-- Links -->
      <div id="top-footer-links">
        <div id="footer-links-area">
          <div>
            <!-- Prima Colonna -->
            <div class="links-col">
              <h3>DC COMICS</h3>
              <ul>
                <li v-for="link in dcComicsLinks" :key="link.text">
                  <a :href="link.url">{{ link.text }}</a>
                </li>
              </ul>
              <h3>SHOP</h3>
              <ul>
                <li v-for="link in shopLinks" :key="link.text">
                  <a :href="link.url">{{ link.text }}</a>
                </li>
              </ul>
            </div>

            <!-- Seconda Colonna -->
            <div class="links-col">
              <h3>DC</h3>
              <ul>
                <li v-for="link in dcLinks" :key="link.text">
                  <a :href="link.url">{{ link.text }}</a>
                </li>
              </ul>
            </div>

            <!-- Terza Colonna -->
            <div class="links-col">
              <h3>SITES</h3>
              <ul>
                <li v-for="link in sitesLinks" :key="link.text">
                  <a :href="link.url">{{ link.text }}</a>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>

      <!-- Footer Logo -->
      <div id="top-footer-logo">
        <figure>
          <img src="../assets/img/dc-logo-bg.png" alt="footer-logo" />
        </figure>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TheTopFooter",
  data() {
    return {
      dcComicsLinks: [
        {
          text: "Characters",
          url: "#",
        },
        {
          text: "Comics",
          url: "#",
        },
        {
          text: "Movies",
          url: "#",
        },
        {
          text: "TV",
          url: "#",
        },
        {
          text: "Games",
          url: "#",
        },
        {
          text: "Videos",
          url: "#",
        },
        {
          text: "News",
          url: "#",
        },
      ],
      shopLinks: [
        {
          text: "Shop DC",
          url: "#",
        },
        {
          text: "Shop DC Collectibles",
          url: "#",
        },
      ],
      dcLinks: [
        {
          text: "Terms Of Use",
          url: "#",
        },
        {
          text: "Privacy policy (New)",
          url: "#",
        },
        {
          text: "Ad Choices",
          url: "#",
        },
        {
          text: "Advertising",
          url: "#",
        },
        {
          text: "Jobs",
          url: "#",
        },
        {
          text: "Subscriptions",
          url: "#",
        },
        {
          text: "Talent Workshops",
          url: "#",
        },
        {
          text: "CPSC Certificates",
          url: "#",
        },
        {
          text: "Ratings",
          url: "#",
        },
        {
          text: "Shop Help",
          url: "#",
        },
        {
          text: "Contact Us",
          url: "#",
        },
      ],
      sitesLinks: [
        {
          text: "DC",
          url: "#",
        },
        {
          text: "MAD Magazine",
          url: "#",
        },
        {
          text: "DC Kids",
          url: "#",
        },
        {
          text: "DC Universe",
          url: "#",
        },
        {
          text: "DC Power Visa",
          url: "#",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.container {
  height: 100%;
}

// Rendendolo dispolay flex consentiamo di scomporre
// il top-footer in due diverse aree: area logo e area links
#top-footer {
  display: flex;
  height: 100%;

  // Diamo il position relative per posizionare il bottom footer
  position: relative;

  // Centriamo la foto e diamo height: 100 al figure così da ereditare
  // l'altezza del footer
  figure {
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }
}

// Entrambe le aree occuperanno il 50%
#top-footer-links,
#top-footer-logo {
  flex-basis: 50%;
}

#top-footer-links {
  // Lo rendiamo flex in modo da affiancare mano mano
  // le liste di links
  display: flex;

  // Area dove si troveranno i links
  #footer-links-area {
    display: flex;
    align-items: center;

    margin: 0;

    // Diamo un po di margine a destra delle colonne dei link
    .links-col {
      margin-right: 50px;
    }
  }

  #footer-links-area > div {
    display: flex;
  }

  h3 {
    color: white;
    font-size: 1rem;
    font-weight: bold;

    margin-bottom: 1rem;
  }
  ul {
    li {
      margin-bottom: 10px;

      a {
        color: gray;
      }
    }
  }
}
</style>
