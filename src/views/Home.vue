<template>
  <div class="main">
    <h1>Gallery</h1>
    <album-gallery/>
  </div>
</template>

<script>
import AlbumGallery from '@/components/AlbumGallery.vue'

export default {
  name: 'Home',
  components: {
    AlbumGallery
  }
}
</script>
