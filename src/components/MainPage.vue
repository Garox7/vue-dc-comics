<template>
  <main>
    <div class="main__container">
      <h1>Content goes here</h1>
    </div>
  </main>
</template>

<script>
export default {
  name: 'MainPage',
};
</script>

<style lang="scss" scoped>
main {
  background-color: #212529;
  display: flex;
  justify-content: center;
}

.main__container {
  color: white;
  flex: 1 1 auto;
  max-width: 900px;
  padding: 2rem 0;
}
</style>
