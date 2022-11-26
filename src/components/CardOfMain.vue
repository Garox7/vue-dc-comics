<template>
  <div> <!-- class="card" in MainPage -->
    <div class="cover__img">
      <img
        :src="card.thumb"
        :alt="card.series"
      >
    </div>
    <p>{{ card.type }}</p>
  </div>
</template>

<script>
export default {
  name: 'CardOfMain',
  props: {
    card: Object,
  },
};
</script>

<style lang="scss" scoped>
.cover__img {
  height: 150px;
  margin-bottom: 10px;

  img {
    width: 100%;
    max-height: 100%;
    object-position: top;
    object-fit: cover;
  }

  p {
    text-transform: uppercase;
  }
}

</style>
