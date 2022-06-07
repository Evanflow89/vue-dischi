<template>
  <div class="album">
    <img :src="album.poster" :alt="album.title" />
    <h2>{{ album.title }}</h2>
    <div>{{ album.author }}</div>
    <span>{{ album.year }}</span>
  </div>
</template>

<script>
export default {
  name: "CardAlbum",
  props: {
    album: Object,
  },
};
</script>

<style lang="scss">
.album {
  background-color: var(--primary-color);
  color: var(--text-color);
}
</style>