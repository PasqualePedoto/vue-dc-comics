<template>
  <header>
    <div id="top-header"></div>
    <div id="bottom-header">
      <div class="container">
        <nav id="header-content">
          <div id="logo">
            <figure>
              <img src="../assets/img/dc-logo.png" alt="DC-logo" />
            </figure>
          </div>
          <div id="list-of-links">
            <ul>
              <li v-for="link in links" :key="link.text">
                <a :href="link.url">{{ link.text }}</a>
              </li>
            </ul>
          </div>
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

  height: 150px;
}

#bottom-header > * {
  height: 100%;
}

#header-content {
  display: flex;
  align-items: center;
  justify-content: space-between;

  padding: 10px;
}

#header-content {
  padding: 0;
}

#logo {
  display: flex;
  align-items: center;
  justify-content: center;
}

#logo,
#header-content,
#list-of-links {
  height: 100%;
}

ul {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
  cursor: pointer;

  li {
    height: 100%;
    padding: 0 1rem;
    border-bottom: 10px solid transparent;
    transition: border-bottom 0.2s linear;

    a {
      height: 100%;

      display: flex;
      align-items: center;
      justify-content: center;
    }
  }
}

ul li:hover {
  border-bottom: 10px solid #1c82fa;
}

ul li:hover a {
  color: #1c82fa;
}
</style>
