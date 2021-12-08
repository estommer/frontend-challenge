<template>
  <div class="album-card">
    <h1>{{title}}</h1>
    <album-cover :cover = "cover"/>
    <album-info :release = "release" :price = "price"/>
  </div>
</template>

<script>
import AlbumCover from '@/components/AlbumCover.vue'
import AlbumInfo from '@/components/AlbumInfo.vue'

export default {
  name: 'album-card',
  props: {
    album: {
      type: Object,
			required: true,
		},
  },
  components: {
    AlbumCover,
    AlbumInfo
  },
  data() {
    return {
      title: this.album.title.label,
      cover: this.album['im:image'][2].label,
      release: this.album['im:releaseDate'].attributes.label,
      price: this.album['im:price'].label
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