<template>
  <div>
    <HeaderPage />

    <MainPage />

    <ItemsWrapper />
  </div>
</template>

<script>
import HeaderPage from '@/components/HeaderPage.vue';
import MainPage from '@/components/MainPage.vue';
import ItemsWrapper from '@/components/ItemsWrapper.vue';

export default {
  components: {
    HeaderPage,
    MainPage,
    ItemsWrapper,
  },
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=PT+Sans+Narrow:wght@400;700&display=swap');

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html {
  font-family: 'PT Sans Narrow', sans-serif;
}

body {
  width: 100%;
  height: 100%;
}

a {
  text-decoration: none;
}
</style>
