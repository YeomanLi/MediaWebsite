<template>
  <div class="medias-box">
    <div class="container">
      <template v-for="media in mediaList">
        <media-item :media="media"></media-item>
      </template>
    </div>
  </div>
</template>

<script>
import MediaItem from "./MediaItem.vue";
export default {
  name: "media-list",
  created() {
    if (0 === this.mediaList.length) {
      this.$store.dispatch("allMedias");
    }
  },
  computed: {
    mediaList() {
      return this.$store.getters.allMedias;
    }
  },
  data() {
    return {};
  },
  components: {
    "media-item": MediaItem
  }
};
</script>

<style scoped>
.medias-box {
  background: #f7f8fb;
  padding: 30px 0;
}
</style>
