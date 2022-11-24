<template>
<header>
  <div class="header__container">
    <img src="@/img/dc-logo.png" alt="Logo">
    <nav>
      <ul>
        <li><a href="#!">characters</a></li>
        <li><a href="#!">comics</a></li>
        <li><a href="#!">movies</a></li>
        <li><a href="#!">tv</a></li>
        <li><a href="#!">games</a></li>
        <li><a href="#!">collectibles</a></li>
        <li><a href="#!">videos</a></li>
        <li><a href="#!">fans</a></li>
        <li><a href="#!">news</a></li>
        <li><a href="#!">shop</a></li>
      </ul>
    </nav>
  </div>
</header>
</template>

<script>
export default {
  name: 'HeaderPage',
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
