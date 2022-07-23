<template>
  <main>
    <div id="content">
      <div class="container">
        <h2>Content is here</h2>
      </div>
    </div>
    <div id="merch">
      <div class="container">
        <ul>
          <!-- Comics -->
          <li>
            <a href="#">
              <figure>
                <img src="../assets/img/buy-comics-digital-comics.png" alt="comics" />
              </figure>
            </a>
            <p>DIGITAL COMICS</p>
          </li>
          <!-- DC Comics -->
          <li>
            <a href="#">
              <figure>
                <img src="../assets/img/buy-comics-merchandise.png" alt="dc-comics" />
              </figure>
            </a>
            <p>DC MERCHANDIZING</p>
          </li>
          <!-- Shop -->
          <li>
            <a href="#">
              <figure>
                <img src="../assets/img/buy-comics-shop-locator.png" alt="shop" />
              </figure>
            </a>
            <p>SUBSCRIPTION</p>
          </li>
          <!-- Subscriptions -->
          <li>
            <a href="#">
              <figure>
                <img src="../assets/img/buy-comics-subscriptions.png" alt="sub" />
              </figure>
            </a>
            <p>COMIC SHOP LOCATOR</p>
          </li>
          <!--  -->
          <li>
            <a href="#">
              <figure>
                <img src="../assets/img/buy-dc-power-visa.svg" alt="visa" />
              </figure>
            </a>
            <P>DC POWER VISA</P>
          </li>
        </ul>
      </div>
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
  flex-shrink: 0;

  #content {
    padding: 50px;
    background-color: black;

    position: relative;

    h2 {
      font-weight: bold;
      color: white;
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
