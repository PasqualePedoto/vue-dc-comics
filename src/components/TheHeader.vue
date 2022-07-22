<template>
  <header>
    <div id="top-header"></div>
    <div id="bottom-header">
      <div class="container">
        <div class="border">
          <figure>
            <img src="../assets/img/dc-logo.png" alt="DC-logo" />
          </figure>
          <ul>
            <li v-for="link in links" :key="link.text">
              <a :href="link.url">{{ link.text }}</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "TheHeader",
  data() {
    return {
      links: [
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

<style scoped lang="scss">
#top-header {
  background-color: black;
  padding: 10px;
  width: 100%;
}

#bottom-header {
  background-color: white;
}

.container > div {
  display: flex;
  align-items: center;
  justify-content: space-between;

  padding: 10px;
  height: 100%;
}

ul {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;

  li {
    height: 100%;
    margin-right: 1.5rem;

    a {
      height: 100%;
    }
  }
}
</style>
