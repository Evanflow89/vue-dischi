<template>
  <header>
    <div class="logo">
      <img src="../../assets/img/spotify-logo.png" alt="logo Spotify" />
    </div>
    <div class="select-bar">
      <Select />
    </div>
  </header>
</template>

<script>
import Select from "../commons/Select.vue";
export default {
  name: "BaseHeader",
  components: {
    Select,
  },
};
</script>

<style lang="scss">
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: var(--primary-color);
  padding: 0.625rem 0.625rem;
  margin-bottom: 3.125rem;
  .logo img {
    max-width: 3.125rem;
  }
}
</style>