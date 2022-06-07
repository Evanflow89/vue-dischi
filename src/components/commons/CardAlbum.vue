<template>
  <div class="album">
    <img src="https://via.placeholder.com/300" alt="" />
    <h2>Titolo Album</h2>
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
  color: var(--primary-color);
}
</style>