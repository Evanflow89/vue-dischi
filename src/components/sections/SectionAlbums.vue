<template>
  <section>
    <div class="container">
      <div class="row">
        <card-album
          class="col-lg-2 m-4 flex-wrap"
          v-for="(album, index) in albums"
          :key="index"
          :album="album"
        />
      </div>
    </div>
  </section>
</template>

<script>
import axios from "axios";
import CardAlbum from "../commons/CardAlbum.vue";

export default {
  components: { CardAlbum },
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
        this.albums = response.data.response;
      })
      .catch((error) => {
        // handle error
        console.log(error);
      });
  },
};
</script>

<style lang="scss">
</style>