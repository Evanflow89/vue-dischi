<template>
  <section>
    <div class="container">
      <div class="row"></div>
    </div>
  </section>
</template>

<script>
import axios from "axios";

export default {
  name: "SectionAlbums",
  data() {
    return {
      albums: [],
    };
  },

  created() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((response) => {
        // handle success
        this.albums = response.response.data;
      })
      .catch((error) => {
        // handle error
        console.log(error);
      });
  },
};
</script>

<style>
</style>