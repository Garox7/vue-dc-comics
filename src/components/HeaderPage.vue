<template>
<header>
  <div class="header__container">
    <img src="@/img/dc-logo.png" alt="Logo">
    <nav class="desktop__nav">
      <ul>
        <li v-for="eleMenu in arrMenu" :key="eleMenu.text">
          <a :href="eleMenu.href">{{ eleMenu.text }}</a>
        </li>
      </ul>
    </nav>
    <div class="mobile__menu__toggle">
      <button @click="toggleMenu()">
        <span class="material-symbols-outlined">menu</span>
      </button>
    </div>
    <div class="mobile__nav" v-show="isExpanded">
      <button @click="toggleMenu()">
        <span class="material-symbols-outlined">close</span>
      </button>
      <ul>
        <li v-for="eleMenu in arrMenu" :key="eleMenu.text">
          <a :href="eleMenu.href">{{ eleMenu.text }}</a>
        </li>
      </ul>
    </div>
  </div>
</header>
</template>

<script>
export default {
  name: 'HeaderPage',
  data() {
    return {
      arrMenu: [
        {
          url: '#!',
          text: 'characters',
        },
        {
          url: '#!',
          text: 'comics',
        },
        {
          url: '#!',
          text: 'movies',
        },
        {
          url: '#!',
          text: 'tv',
        },
        {
          url: '#!',
          text: 'games',
        },
        {
          url: '#!',
          text: 'collectables',
        },
        {
          url: '#!',
          text: 'videos',
        },
        {
          url: '#!',
          text: 'fans',
        },
        {
          url: '#!',
          text: 'news',
        },
        {
          url: '#!',
          text: 'shop',
        },
      ],
      isExpanded: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isExpanded = !this.isExpanded;
    },
  },
};
</script>

<style lang="scss" scoped>
$header-heigth: 80px;
$link-color: #0d6efd;

header {
  background-color: white;
  height: $header-heigth;
  width: 100%;
  display: flex;
  align-content: center;
  justify-content: center;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 10;

  .header__container {
    flex: 1 1 auto;
    max-width: 1025px;
    padding: 0 10px;
    display: flex;
    justify-content: space-between;
    align-items: center;

    img {
      width: 55px;
      height: 55px;
    }

    .desktop__nav {
      height: 100%;

      ul {
        list-style: none;
        display: flex;
        align-items: center;
        flex-wrap: wrap;
        gap: 1.2rem;
        height: 100%;

        li {
          height: 100%;
          display: flex;
          align-items: center;

          a {
            color: black;
            font-weight: bold;
            height: 95%;
            display: flex;
            align-items: center;
            text-transform: uppercase;

            &:hover {
              color: $link-color;
              border-bottom: 3px solid $link-color;
              margin-bottom: -3px;
            }
          }
        }
      }
    }

    .mobile__menu__toggle {
      display: none;
    }
  }
}

@media screen and (max-width: 768px) {
  header .header__container .desktop__nav {
    display: none;
  }
  header .header__container .mobile__menu__toggle {
    display: block;

  }

  button {
    background-color: transparent;
    border: 1px solid black;
    border-radius: 5px;
    padding: .5rem;
    display: flex;
  }
  .mobile__nav {
    background-color: white;
    position: fixed;
    width: 70vw;
    top: 0;
    bottom: 0;
    right: 0;
    display: flex;
    flex-direction: column;
    box-shadow: -2px 2px 3px 2px rgba(0 0 0 / .2);

    button {
      align-self: flex-end;
      margin: 1.2rem .6rem;
    }

    ul {
      margin-top: 1rem;
      display: flex;
      flex-direction: column;
      align-items: center;

      li {
        list-style: none;
        margin-bottom: 1rem;

        a {
          font-size: 16px;
          font-weight: bold;
          text-transform: uppercase;
        }
      }
    }

  }
}
</style>
