<template>
  <div>
    <div class="cover__img">
      <img
        :src="cover.thumb"
        :alt="cover.series"
      >
    </div>

    <p class="title">{{ cover.series }}</p>
  </div>
</template>

<script>
export default {
  name: 'CardOfMain',
  props: {
    cover: Object,
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
}

.title {
  font-size: 14px;
  text-transform: uppercase;
}
</style>
