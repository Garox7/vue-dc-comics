<template>
<header>
  <div class="header__container">
    <img src="@/img/dc-logo.png" alt="Logo">
    <nav>
      <ul>
        <li v-for="eleMenu in arrMenu" :key="eleMenu.text">
          <a :href="eleMenu.href">{{ eleMenu.text }}</a>
        </li>
      </ul>
    </nav>
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
    };
  },
};
</script>

<style lang="scss" scoped>
$header-heigth: 80px;
$link-color: #0d6efd;

header {
  flex: 1 1 auto;
  height: $header-heigth;
  width: 100%;
  display: flex;
  align-content: center;
  justify-content: center;

  .header__container {
    flex: 1 1 auto;
    max-width: 900px;
    display: flex;
    justify-content: space-between;
    align-items: center;

    img {
      width: 65px;
      height: 65px;
    }

    nav {
      height: 100%;

      ul {
        list-style: none;
        display: flex;
        align-items: center;
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
  }
}
</style>
