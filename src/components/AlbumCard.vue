<template>
  <div class="album-card">
    <h1>{{name}}</h1>
    <album-cover :cover = "cover"/>
  </div>
</template>

<script>
import AlbumCover from '@/components/AlbumCover.vue'

export default {
  name: 'album-card',
  props: {
    album: {
      type: Object,
			required: true,
		},
  },
  components: {
    AlbumCover
  },
  data() {
    return {
      name: this.album['im:name'].label,
      cover: this.album['im:image'][2].label
    }
  },
}
</script>

<style scoped lang="scss">
.album-card {
  width: 400px;
  height: 400px;
  background-color: orange;
}
</style>