<template>
  <div>
    <div class="title">
      <h1>
        <i class="fa fa-braille"></i> 媒体存档
      </h1>
    </div>
    <media-list></media-list>
  </div>
</template>

<script>
// @ is an alias to /src
import MediaList from "@/components/MediaList.vue";
export default {
  name: "home",
  components: {
    "media-list": MediaList
  }
};
</script>
