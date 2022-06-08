<template>
  <div>
    <form class="d-flex" @submit.prevent="$emit('searching', Select)">
      <select name="select-genre" id="genre">
        <option value="rock">Rock</option>
        <option value="pop">Pop</option>
        <option value="jazz">Jazz</option>
        <option value="metal">Metal</option>
      </select>
    </form>
  </div>
</template>

<script>
export default {
  name: "Select-bar",
};
</script>

<style lang="scss">
select {
  width: 12.5rem;
  margin-right: 1.25rem;
}
</style>