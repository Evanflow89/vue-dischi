<template>
  <div>
    <form class="d-flex" @submit.prevent="$emit('searching', selectValue)">
      <select name="select-genre" id="genre" v-model="selectValue">
        <option value="all">All</option>
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
  data() {
    return {
      selectValue: "",
    };
  },
};
</script>

<style lang="scss">
select {
  width: 12.5rem;
  margin-right: 1.25rem;
}
</style>