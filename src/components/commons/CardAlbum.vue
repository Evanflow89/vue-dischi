<template>
  <div class="album">
    <img :src="album.poster" alt="" />
    <h2>{{ album.title }}</h2>
    <div>Nome della Band</div>
    <span>Anno Uscita</span>
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