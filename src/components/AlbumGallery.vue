<template>
  <div class="album-gallery">
    <album-card v-for="(album, index) of albums" :key="index" :album="album"/>
  </div>
</template>

<script>
import AlbumCard from '@/components/AlbumCard.vue'

export default {
  name: 'album-gallery',
  props: {},
  components: {
    AlbumCard
  },
  data() {
    return {
      albums: []
    }
  },
  created(){
    fetch("https://itunes.apple.com/us/rss/topalbums/limit=100/json")
      .then(response => response.json())
      .then(data => {
        this.albums = data.feed.entry;
        console.log(data.feed.entry[3]);
      });
  }
}
</script>

<style scoped lang="scss">
.album-gallery {
  display: flex;
  flex-wrap: wrap;
  background-color: #42b983;
}
</style>