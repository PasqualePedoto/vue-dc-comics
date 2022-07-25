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
            <li v-for="(link, i) in NavbarLinks" :key="i">
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
  props: {
    NavbarLinks: Array,
  },
};
</script>

<style lang="scss" scoped>
header {
  flex-shrink: 0;
}
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
        width: 80px;
        padding: 0 0.5rem;

        display: flex;
        align-items: center;
        justify-content: center;

        border-bottom: 5px solid transparent;
        transition: border-bottom 0.15s linear;

        cursor: pointer;

        a {
          color: black;
          transition: color 0.15s linear;
        }
      }

      li:hover {
        border-bottom: 5px solid #1c82f9;
      }

      li:hover a {
        color: #1c82f9;
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
