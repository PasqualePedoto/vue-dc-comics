<template>
  <header>
    <!-- Top Header - Bgc Black -->
    <div id="top-header">
      <div class="container"></div>
    </div>
    <!-- Bottom Header - Navbar -->
    <div id="bottom-header">
      <div class="container">
        <!-- Navbar -->
        <nav>
          <!-- DC Logo -->
          <figure>
            <img src="../assets/img/dc-logo.png" alt="dc-logo" />
          </figure>

          <!-- Navbar links -->
          <ul>
            <li v-for="link in navbarLinks" :key="link.text">
              <a :href="link.url">{{ link.text }}</a>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "TheHeader",
  data() {
    return {
      navbarLinks: [
        {
          text: "Characters",
          url: "#",
          current: false,
        },
        {
          text: "Comics",
          url: "#",
          current: true,
        },
        {
          text: "Movies",
          url: "#",
          current: false,
        },
        {
          text: "TV",
          url: "#",
          current: false,
        },
        {
          text: "Games",
          url: "#",
          current: false,
        },
        {
          text: "Collectibles",
          url: "#",
          current: false,
        },
        {
          text: "Videos",
          url: "#",
          current: false,
        },
        {
          text: "Fans",
          url: "#",
          current: false,
        },
        {
          text: "News",
          url: "#",
          current: false,
        },
        {
          text: "Shop",
          url: "#",
          current: false,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
// Definiamo il bgc del top-header
#top-header {
  background-color: black;
  padding: 10px;
}

// Ereditiamo l'altezza del bottom-header
// cosi da cambiare il display in flex
.container {
  height: 100%;
}

// Definiamo il bottom-header
#bottom-header {
  background-color: #fff;
  height: 150px;

  //Centriamo la Navbar
  .container > div {
    display: flex;
    align-items: stretch;
    width: 100%;

    // Facciamo ereditare l'altezza
    height: 100%;
  }

  // Navbar
  nav {
    display: flex;
    justify-content: space-between;
    height: 100%;

    // Rendiamo flex sia il figure che l'ul cosi da centrare tutto
    ul {
      display: flex;

      li {
        margin-right: 1.2rem;

        display: flex;
        align-items: center;
        justify-content: center;

        border-bottom: transparent;

        a {
          color: black;
        }
      }
    }

    figure {
      display: flex;
      align-items: center;
      justify-content: center;
    }
  }
}
</style>
