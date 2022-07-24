<template>
  <div id="bottom-footer">
    <div id="social-links">
      <div class="container">
        <div>
          <button>SIGN-UP NOW!</button>
          <div id="social">
            <!-- Lista di figure -->
            <ul>
              <li class="follow-us">FOLLOW US</li>
              <li v-for="social in socialLinks" :key="social.src">
                <a :href="social.url">
                  <img :src="social.src" :alt="social.alt" />
                </a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <div class="black-area">
      <div class="container"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TheBottomFooter",
  data() {
    return {
      socialLinks: [
        {
          src: `${require("../assets/img/footer-youtube.png")}`,
          alt: "youtube",
          url: "#",
        },
        {
          src: `${require("../assets/img/footer-twitter.png")}`,
          alt: "twitter",
          url: "#",
        },
        {
          src: `${require("../assets/img/footer-pinterest.png")}`,
          alt: "pinterest",
          url: "#",
        },
        {
          src: `${require("../assets/img/footer-facebook.png")}`,
          alt: "facebook",
          url: "#",
        },
        {
          src: `${require("../assets/img/footer-periscope.png")}`,
          alt: "periscope",
          url: "#",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
//Rendiamo flex l'area dei social links
.container > div {
  display: flex;
  justify-content: space-between;
}

#bottom-footer {
  // Coordinate che posizionano in basso il bottom header
  position: absolute;
  bottom: 0;
  right: 0;
  left: 0;

  #social-links {
    background-color: #303030;
    padding: 20px 0;

    #social ul {
      display: flex;
      height: 100%;

      .follow-us {
        color: #1c82f9;
        font-size: 1.5rem;
        font-weight: bold;

        margin-right: 1rem;
      }

      li {
        display: flex;
        align-items: center;

        margin-right: 1rem;
      }

      figure {
        margin-right: 1rem;
      }
    }
  }

  button {
    background-color: #303030;
    border: 2px solid #1c82f9;
    padding: 20px;

    font-size: 1rem;
    color: white;

    cursor: pointer;
  }

  .black-area {
    padding: 10px;

    background-color: black;
  }
}
</style>
