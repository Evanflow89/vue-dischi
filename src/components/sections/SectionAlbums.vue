<template>
  <section>
    <div class="container mb-4">
      <div class="row d-flex justify-content-center">
        <card-album
          class="col-12 col-md-6 col-lg-2 m-3 flex-wrap"
          v-for="(album, index) in AlbumsFilter"
          :key="index"
          :album="album"
        />
      </div>
    </div>
  </section>
</template>

<script>
import axios from "axios";
import DataShared from "../../shared/DataShared";
import CardAlbum from "../commons/CardAlbum.vue";

export default {
  components: { CardAlbum },
  name: "SectionAlbums",
  data() {
    return {
      DataShared,
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
  computed: {
    AlbumsFilter() {
      return this.albums.filter((elm) => {
        return elm.genre
          .toLowerCase()
          .includes(this.DataShared.selectValue.toLowerCase());
      });
    },
  },
};
</script>

<style lang="scss">
</style>