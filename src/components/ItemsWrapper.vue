<template>
  <section>
    <div class="items__container">
      <div class="item">
        <img src="@/img/buy-comics-digital-comics.png" alt="Digital Comics">
        <h4>digital comics</h4>
      </div>
      <div class="item">
        <img src="@/img/buy-comics-merchandise.png" alt="Comics Merchandise">
        <h4>dc merchandise</h4>
      </div>
      <div class="item">
        <img src="@/img/buy-comics-subscriptions.png" alt="Comics Subscriptions">
        <h4>subscriptions</h4>
      </div>
      <div class="item">
        <img src="@/img/buy-comics-shop-locator.png" alt="Shop Locator">
        <h4>comic shop locator</h4>
      </div>
      <div class="item">
        <img src="@/img/buy-dc-power-visa.svg" alt="Power Visa">
        <h4>dc power visa</h4>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ItemsWrapper',
};
</script>

<style lang="scss" scoped>
section {
  background-color: rgb(56, 128, 241);
  width: 100%;
}

.items__container {
  max-width: 1025px;
  margin: 0 auto;
  padding: 3rem 0;
  display: flex;
  align-items: center;
  justify-content: space-around;

  .item {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: .5rem;

    &:last-child img {
      height: 30px;
    }

    img {
      height: 45px;
    }

    h4 {
      color: white;
      font-size: 14px;
      font-weight: 400;
      text-transform: uppercase;
    }
  }
}
</style>
